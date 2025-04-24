<script>
</script>

<div class="kirjautuminen">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"
    ><path
      d="M224 256A128 128 0 1 0 224 0a128 128 0 1 0 0 256zm-45.7 48C79.8 304 0 383.8 0 482.3C0 498.7 13.3 512 29.7 512l388.6 0c16.4 0 29.7-13.3 29.7-29.7C448 383.8 368.2 304 269.7 304l-91.4 0z"
    /></svg
  >
  <a href="#">Kirjaudu / Luo tili</a>
</div>

<style>
  .kirjautuminen {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    vertical-align: middle;
    gap: 10px;
    padding: 8px 4px;
    margin-left: 30px;
  }

  .kirjautuminen:hover {
    background-color: #fff;
  }

  .kirjautuminen svg {
    fill: #fff;
    width: 18px;
    height: 18px;
    cursor: pointer;
  }

  .kirjautuminen:hover svg {
    fill: var(--väri-tausta-tumma);
    width: 18px;
    height: 18px;
    cursor: pointer;
  }

  a:link {
    text-decoration: none;
    color: #fff;
    font-size: 0.9rem;
  }

  .kirjautuminen:hover a:any-link {
    text-decoration: none;
    color: var(--väri-tausta-tumma);
  }

  a:active {
    text-decoration: none;
    color: #fff;
  }

  a:visited {
    text-decoration: none;
    color: #fff;
  }
</style>
