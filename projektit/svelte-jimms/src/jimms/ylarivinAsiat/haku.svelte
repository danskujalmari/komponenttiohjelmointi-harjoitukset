<script>
</script>

<div class="haku">
  <input type="text" placeholder="Hae tuotteista" />
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"
    ><!--!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.--><path
      d="M416 208c0 45.9-14.9 88.3-40 122.7L502.6 457.4c12.5 12.5 12.5 32.8 0 45.3s-32.8 12.5-45.3 0L330.7 376c-34.4 25.2-76.8 40-122.7 40C93.1 416 0 322.9 0 208S93.1 0 208 0S416 93.1 416 208zM208 352a144 144 0 1 0 0-288 144 144 0 1 0 0 288z"
    /></svg
  >
</div>

<style>
  .haku {
    display: flex;
    position: relative;
    align-items: center;
    width: 100%;
  }

  .haku input {
    color: #fff;
    padding: 13px 35px;
    font-size: 1rem;
    background-color: #1a1e21;
    border: 1px solid #3f4144;
    border-radius: 4px;
    width: 100%;
    transition: border-color 0.2s ease;
  }

  .haku input:focus {
    outline: none;
    border-color: var(--väri-linkki-tausta-hover);
  }

  .haku input::placeholder {
    color: #8b8b8b;
  }

  .haku svg {
    width: 18px;
    height: 18px;
    fill: #ee6622;
    position: absolute;
    left: 10px;
    pointer-events: none;
  }

  @media screen and (min-width: 1400px) {
    .haku input {
      padding: 15px 45px;
      font-size: 1.1rem;
    }

    .haku svg {
      width: 22px;
      height: 22px;
      left: 15px;
    }
  }

  @media screen and (max-width: 390px) {
    .haku input {
      padding: 10px 35px;
      font-size: 14px;
    }

    .haku svg {
      width: 16px;
      height: 16px;
    }
  }
</style>
