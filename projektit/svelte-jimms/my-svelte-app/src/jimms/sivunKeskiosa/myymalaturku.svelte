<div class="wrapper">
  <div class="myymala">
    <h2>Myymälä Turku</h2>
    <div class="aikaosio">
      <div class="ajat1 ajat">
        <ul>
          <li>Ma-Pe</li>
          <li>11:00-19:00</li>
        </ul>
      </div>
      <div class="ajat2 ajat">
        <ul>
          <li>La</li>
          <li>10:00-16:00</li>
        </ul>
      </div>
    </div>
    <div class="texti">
      Maksuvälineenä käyvät yleisimmät pankki- ja luottokortit sekä
      mobiilimaksutavat. Ei käteismaksumahdollisuutta.
    </div>
    <div class="osoite">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 384 512"
        ><!--!Font Awesome Free 6.7.2 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license/free Copyright 2025 Fonticons, Inc.--><path
          d="M215.7 499.2C267 435 384 279.4 384 192C384 86 298 0 192 0S0 86 0 192c0 87.4 117 243 168.3 307.2c12.3 15.3 35.1 15.3 47.4 0zM192 128a64 64 0 1 1 0 128 64 64 0 1 1 0-128z"
        /></svg
      >
      <a href="#">Lukkosepänkatu 7 <br /> 20320 Turku</a>
    </div>
  </div>
</div>

<style>
  .wrapper {
    max-width: 350px;
    display: flex;
    flex-direction: column;
  }

  .myymala {
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .osoite {
    display: flex;
    gap: 8px;
  }
  .ajat ul {
    display: flex;
    gap: 30%;
    color: var(--väri-teksti);
  }

  .texti {
    color: var(--väri-teksti);
  }

  svg {
    fill: var(--väri-linkki-tausta-hover);
  }

  a:any-link {
    color: var(--väri-teksti);
    text-decoration: none;
  }

  a:hover {
    color: var(--väri-linkki-tausta-hover);
  }
</style>
