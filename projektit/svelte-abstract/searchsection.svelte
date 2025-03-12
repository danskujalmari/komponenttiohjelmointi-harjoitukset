<div class="search_section">
  <div class="input-container">
    <h1>How can we help?</h1>
    <input type="text" placeholder="Search" />
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
      <path
        d="M438.6 278.6c12.5-12.5 12.5-32.8 0-45.3l-160-160c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L338.8 224 32 224c-17.7 0-32 14.3-32 32s14.3 32 32 32l306.7 0L233.4 393.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0l160-160z"
      />
    </svg>
  </div>
</div>

<style>
  .search_section {
    padding: 110px 300px;
    margin: 0 auto;
    background-color: var(--väri-neljas);
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
  }

  .input-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    position: relative;
  }

  .search_section h1 {
    text-transform: none;
    font-size: 4.3rem;
    font-weight: 500;
    margin: 0;
  }

  .search_section input {
    padding: 1rem 2rem 1rem 1rem;
    font-size: 1.2rem;
    border: 1px solid var(--väri-toka);
    border-radius: 4px;
    width: 600px;
  }

  svg {
    position: absolute;
    right: 15px;
    top: 82%;
    transform: translateY(-50%);
    width: 20px;
    height: 20px;
  }

  @media (max-width: 375px) {
    .search_section h1 {
      font-size: 2.3rem;
    }

    .search_section {
      padding: 50px 0;
    }

    .search_section input {
      padding: 0.5rem 1rem 0.5rem 1rem;
    }

    svg {
      position: absolute;
      right: 15px;
      top: 81%;
      transform: translateY(-50%);
      width: 20px;
      height: 20px;
    }

    .search_section input {
      padding: 0.7rem 2rem 0.7rem 1rem;
      font-size: 1.2rem;
      border: 1px solid var(--väri-toka);
      border-radius: 4px;
      width: 320px;
    }
  }
</style>
