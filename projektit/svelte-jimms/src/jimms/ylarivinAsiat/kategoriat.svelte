<script>
  import Kategoria from "./kategoria.svelte";
</script>

<div class="kategoriat-wrapper">
  <ul class="kategoriat">
    <li><Kategoria nimi="tietokone" url="#" /></li>
    <li><Kategoria nimi="komponentit" url="#" /></li>
    <li><Kategoria nimi="oheislaitteet" url="#" /></li>
    <li><Kategoria nimi="pelaaminen" url="#" /></li>
    <li><Kategoria nimi="sim racing" url="#" /></li>
    <li><Kategoria nimi="verkkotuotteet" url="#" /></li>
    <li><Kategoria nimi="tarvikkeet" url="#" /></li>
    <li><Kategoria nimi="erikoistuotteet" url="#" /></li>
    <li><Kategoria nimi="ohjelmistot" url="#" /></li>
    <li><Kategoria nimi="palvelut" url="#" /></li>
    <li><Kategoria nimi="kampanjat" url="#" /></li>
  </ul>
</div>

<style>
  .kategoriat-wrapper {
    width: 100%;
    overflow-x: auto;
    overflow-y: hidden;
    -webkit-overflow-scrolling: touch;
    scrollbar-width: none;
    -ms-overflow-style: none;
  }

  .kategoriat-wrapper::-webkit-scrollbar {
    display: none;
  }

  .kategoriat {
    list-style: none;
    margin: 0;
    padding: 0 0 0 15px;
    display: flex;
    gap: 15px;
    white-space: nowrap;
  }

  @media screen and (min-width: 1024px) {
    .kategoriat-wrapper {
      display: flex;
      justify-content: center;
      overflow: visible;
    }

    .kategoriat {
      max-width: 1440px;
      width: 100%;
      padding: 0;
      gap: 20px;
    }
  }

  @media screen and (max-width: 390px) {
    .kategoriat {
      padding: 0 0 0 10px;
      gap: 10px;
    }
  }
</style>
