<script>
  let todos = [
    {
      id: "todo-1",
      text: "Create a Svelte starter app",
      completed: true,
      editing: false,
    },
    {
      id: "todo-2",
      text: "Create your first component",
      completed: true,
      editing: false,
    },
    {
      id: "todo-3",
      text: "Complete the rest of the tutorial",
      completed: false,
      editing: false,
    },
  ];
  let newTodoText = "";
  let filter = "all";
  let editText = "";

  function addTodo(event) {
    event.preventDefault();
    if (newTodoText.trim()) {
      todos = [
        ...todos,
        {
          id: `todo-${todos.length + 1}`,
          text: newTodoText,
          completed: false,
          editing: false,
        },
      ];
      newTodoText = "";
    }
  }

  function deleteTodo(id) {
    todos = todos.filter((todo) => todo.id !== id);
  }

  function toggleTodo(id) {
    todos = todos.map((todo) => {
      if (todo.id === id) {
        return { ...todo, completed: !todo.completed };
      }
      return todo;
    });
  }

  function startEditing(todo) {
    editText = todo.text;
    todos = todos.map((t) => ({
      ...t,
      editing: t.id === todo.id,
    }));
  }

  function cancelEditing() {
    todos = todos.map((todo) => ({
      ...todo,
      editing: false,
    }));
    editText = "";
  }

  function saveEdit(todo) {
    if (editText.trim()) {
      todos = todos.map((t) => {
        if (t.id === todo.id) {
          return {
            ...t,
            text: editText,
            editing: false,
          };
        }
        return t;
      });
      editText = "";
    }
  }

  function checkAll() {
    const allCompleted = todos.every((todo) => todo.completed);
    todos = todos.map((todo) => ({ ...todo, completed: !allCompleted }));
  }

  function removeCompleted() {
    todos = todos.filter((todo) => !todo.completed);
  }

  $: filteredTodos =
    filter === "all"
      ? todos
      : filter === "active"
        ? todos.filter((todo) => !todo.completed)
        : todos.filter((todo) => todo.completed);

  $: completedCount = todos.filter((todo) => todo.completed).length;
  $: totalCount = todos.length;
  $: allCompleted = totalCount > 0 && completedCount === totalCount;
</script>

<div class="todoapp stack-large">
  <form on:submit={addTodo}>
    <h2 class="label-wrapper">
      <label for="todo-0" class="label__lg">What needs to be done?</label>
    </h2>
    <input
      type="text"
      id="todo-0"
      bind:value={newTodoText}
      autocomplete="off"
      class="input input__lg"
    />
    <button
      type="submit"
      disabled={!newTodoText.trim()}
      class="btn btn__primary btn__lg"
    >
      Add
    </button>
  </form>

  <div class="filters btn-group stack-exception">
    <button
      class="btn toggle-btn"
      class:active={filter === "all"}
      aria-pressed={filter === "all"}
      on:click={() => (filter = "all")}
    >
      <span class="visually-hidden">Show</span>
      <span>All</span>
      <span class="visually-hidden">tasks</span>
    </button>
    <button
      class="btn toggle-btn"
      class:active={filter === "active"}
      aria-pressed={filter === "active"}
      on:click={() => (filter = "active")}
    >
      <span class="visually-hidden">Show</span>
      <span>Active</span>
      <span class="visually-hidden">tasks</span>
    </button>
    <button
      class="btn toggle-btn"
      class:active={filter === "completed"}
      aria-pressed={filter === "completed"}
      on:click={() => (filter = "completed")}
    >
      <span class="visually-hidden">Show</span>
      <span>Completed</span>
      <span class="visually-hidden">tasks</span>
    </button>
  </div>

  <h2 id="list-heading">
    {completedCount} out of {totalCount} items completed
  </h2>

  <ul role="list" class="todo-list stack-large" aria-labelledby="list-heading">
    {#each filteredTodos as todo (todo.id)}
      <li class="todo">
        <div class="stack-small">
          {#if todo.editing}
            <form
              class="stack-small"
              on:submit|preventDefault={() => saveEdit(todo)}
            >
              <div class="form-group">
                <input
                  type="text"
                  bind:value={editText}
                  id={todo.id}
                  class="todo-text"
                  autocomplete="off"
                />
              </div>
              <div class="btn-group">
                <button type="button" class="btn" on:click={cancelEditing}>
                  Cancel
                </button>
                <button type="submit" class="btn btn__primary"> Save </button>
              </div>
            </form>
          {:else}
            <div class="c-cb">
              <input
                type="checkbox"
                id={todo.id}
                checked={todo.completed}
                on:change={() => toggleTodo(todo.id)}
              />
              <label for={todo.id} class="todo-label">
                {todo.text}
              </label>
            </div>
            <div class="btn-group">
              <button
                type="button"
                class="btn"
                on:click={() => startEditing(todo)}
              >
                Edit
              </button>
              <button
                type="button"
                class="btn btn__danger"
                on:click={() => deleteTodo(todo.id)}
              >
                Delete
              </button>
            </div>
          {/if}
        </div>
      </li>
    {/each}
  </ul>

  <hr />

  <div class="btn-group">
    <button type="button" class="btn btn__primary" on:click={checkAll}>
      {allCompleted ? "Uncheck" : "Check"} all
    </button>
    <button type="button" class="btn btn__primary" on:click={removeCompleted}>
      Remove completed
    </button>
  </div>
</div>

<style>
  /* RESETS */
  *,
  *::before,
  *::after {
    box-sizing: border-box;
  }
  *:focus {
    outline: 3px dashed #228bec;
    outline-offset: 0;
  }
  html {
    font: 62.5% / 1.15 sans-serif;
  }
  h1,
  h2 {
    margin-bottom: 0;
  }
  ul {
    list-style: none;
    padding: 0;
  }
  button {
    border: none;
    margin: 0;
    padding: 0;
    width: auto;
    overflow: visible;
    background: transparent;
    color: inherit;
    font: inherit;
    line-height: normal;
    -webkit-font-smoothing: inherit;
    -moz-osx-font-smoothing: inherit;
    appearance: none;
  }
  button::-moz-focus-inner {
    border: 0;
  }
  button,
  input,
  optgroup,
  select,
  textarea {
    font-family: inherit;
    font-size: 100%;
    line-height: 1.15;
    margin: 0;
  }
  button,
  input {
    overflow: visible;
  }
  input[type="text"] {
    border-radius: 0;
    background-color: #fff;
  }
  body {
    width: 100%;
    max-width: 68rem;
    margin: 0 auto;
    font:
      1.6rem/1.25 Arial,
      sans-serif;
    background-color: #f5f5f5;
    color: #4d4d4d;
  }
  @media screen and (min-width: 620px) {
    body {
      font-size: 1.9rem;
      line-height: 1.31579;
    }
  }
  /*END RESETS*/

  /* GLOBAL STYLES */
  .form-group > input[type="text"] {
    display: inline-block;
    margin-top: 0.4rem;
  }
  .btn {
    padding: 0.8rem 1rem 0.7rem;
    border: 0.2rem solid #4d4d4d;
    cursor: pointer;
    text-transform: capitalize;
    color: #4d4d4d;
    font-size: 1.6rem;
  }
  .btn.toggle-btn {
    border-width: 1px;
    border-color: #d3d3d3;
    font-size: 1.4rem;
    padding: 0.7rem 1rem;
    min-width: 11rem;
  }
  .btn.toggle-btn[aria-pressed="true"] {
    text-decoration: underline;
    border-color: #4d4d4d;
  }
  .btn__danger {
    color: #fff;
    background-color: #ca3c3c;
    border-color: #bd2130;
    font-size: 1.6rem;
  }
  .btn__filter {
    border-color: lightgrey;
  }
  .btn__primary {
    color: #fff;
    background-color: #000;
    border: 3px solid #333;
  }
  .btn__primary:disabled {
    color: darkgrey;
    background-color: #565656;
    border-color: #444;
  }
  .btn__primary:not(.btn__lg) {
    font-size: 1.6rem;
  }
  .btn-group {
    display: flex;
    justify-content: space-between;
  }
  .btn-group > * {
    flex: 1 1 49%;
  }
  .btn-group > * + * {
    margin-left: 0.8rem;
  }
  .label-wrapper {
    margin: 0;
    margin-bottom: 0.5rem;
    flex: 0 0 100%;
    text-align: center;
  }
  .visually-hidden {
    position: absolute !important;
    height: 1px;
    width: 1px;
    overflow: hidden;
    clip: rect(1px 1px 1px 1px);
    clip: rect(1px, 1px, 1px, 1px);
    white-space: nowrap;
  }
  [class*="stack"] > * {
    margin-top: 0;
    margin-bottom: 0;
  }
  .stack-small > * + * {
    margin-top: 1rem;
  }
  .stack-large > * + * {
    margin-top: 2rem;
  }
  @media screen and (min-width: 550px) {
    .stack-small > * + * {
      margin-top: 1rem;
    }
    .stack-large > * + * {
      margin-top: 2rem;
    }
  }
  .stack-exception {
    margin-top: 1.2rem;
    margin-bottom: 1.5rem;
  }
  /* END GLOBAL STYLES */

  .todoapp {
    background: #fff;
    margin: 2rem 0 4rem 0;
    padding: 1rem;
    position: relative;
    box-shadow:
      0 2px 4px 0 rgb(0 0 0 / 20%),
      0 2.5rem 5rem 0 rgb(0 0 0 / 10%);
  }
  @media screen and (min-width: 550px) {
    .todoapp {
      padding: 4rem;
    }
  }
  .todoapp > * {
    max-width: 50rem;
    margin-left: auto;
    margin-right: auto;
  }
  .todoapp > form {
    max-width: 100%;
  }
  .todoapp > h1 {
    display: block;
    max-width: 100%;
    text-align: center;
    margin: 0;
    margin-bottom: 1rem;
  }
  .label__lg {
    line-height: 1;
    font-weight: 400;
    padding: 0;
    margin-bottom: 0.8rem;
    text-align: center;
    font-size: 1.3rem;
    color: #4d4d4d;
  }
  .input__lg {
    padding: 1.5rem;
    border: 2px solid #000;
    background-color: #fff;
    color: #4d4d4d;
    margin-bottom: 1rem;
  }
  .input__lg:focus {
    border-color: #4d4d4d;
    box-shadow: inset 0 0 0 2px;
  }
  [class*="__lg"] {
    display: inline-block;
    width: 100%;
  }
  @media screen and (min-width: 620px) {
    [class*="__lg"] {
      font-size: 2rem;
    }
  }
  .filters {
    width: 100%;
    margin: unset auto;
    max-width: 45rem;
    margin-left: auto;
    margin-right: auto;
  }
  .btn-group.filters {
    justify-content: center;
    gap: 0.4rem;
  }
  .btn-group.filters > * {
    flex: 0 1 auto;
  }
  .btn-group.filters > * + * {
    margin-left: 0.4rem;
  }
  /* Todo item styles */
  .todo {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    align-items: center;
    padding: 0;
    margin: 0;
    margin-top: 2rem;
  }
  .todo:first-child {
    margin-top: 0;
  }
  .stack-small {
    width: 100%;
  }
  .todo-text {
    width: 100%;
    min-height: 4rem;
    padding: 1rem;
    border: 2px solid #000;
    background-color: #fff;
    color: #4d4d4d;
  }
  .todo-text:focus {
    box-shadow: inset 0 0 0 2px;
  }
  /* CHECKBOX STYLES */
  .c-cb {
    box-sizing: border-box;
    font-family: Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    font-weight: 400;
    font-size: 1.6rem;
    line-height: 1.25;
    display: flex;
    align-items: center;
    position: relative;
    min-height: 44px;
    padding: 0;
    margin: 0;
    clear: left;
  }
  .c-cb > input[type="checkbox"] {
    -webkit-font-smoothing: antialiased;
    cursor: pointer;
    position: relative;
    width: 60px;
    height: 60px;
    margin: 0;
    opacity: 0;
  }
  .c-cb > label {
    font-size: inherit;
    font-family: inherit;
    line-height: inherit;
    display: inline-block;
    margin: 0;
    margin-left: 10px;
    padding: 0;
    cursor: pointer;
    touch-action: manipulation;
    color: #4d4d4d;
  }
  .c-cb > label::before {
    content: "";
    position: absolute;
    left: 0;
    top: 0;
    width: 60px;
    height: 60px;
    border: 2px solid currentcolor;
    background: transparent;
  }
  .c-cb > label::after {
    box-sizing: content-box;
    content: "";
    position: absolute;
    left: 16px;
    top: 18px;
    width: 28px;
    height: 16px;
    transform: rotate(-45deg);
    border: solid;
    border-width: 0 0 4px 4px;
    border-top-color: transparent;
    opacity: 0;
    background: transparent;
  }
  .todo-label {
    color: #4d4d4d;
    font-size: 1.4rem;
    margin-left: 0;
    text-align: left;
  }
  .c-cb > input[type="checkbox"]:checked + label::after {
    opacity: 1;
  }
  .c-cb > input[type="checkbox"]:focus + label::before {
    border-width: 3px;
    outline: 3px dashed #228bec;
  }
  .form-group {
    text-align: left;
  }
  .form-group > label {
    margin-left: 0;
    padding-left: 0;
  }
  .btn__lg {
    padding: 0.7rem;
    font-size: 2rem;
  }
  #list-heading {
    color: #4d4d4d;
    font-size: 1.8rem;
    font-weight: 600;
    margin: 1.5rem 0;
    padding: 0;
    text-align: left;
    max-width: 50rem;
    margin-left: auto;
    margin-right: auto;
  }
  .todo-list {
    max-width: 50rem;
    margin-left: auto;
    margin-right: auto;
  }
</style>
