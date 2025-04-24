<script>
  import Otsikko from "./otsikko.svelte";
  import Haku from "./haku.svelte";
  import Toiminnot from "./toiminnot.svelte";
</script>

<div class="ylarivi">
  <div class="ylarivin-sisalto">
    <Otsikko />
    <div class="haku-ryhma">
      <Haku />
    </div>
    <Toiminnot />
  </div>
</div>

<style>
  .ylarivi {
    background-color: var(--väri-tausta-tumma);
    width: 100%;
  }

  .ylarivin-sisalto {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 15vw;
    gap: 30px;
    max-width: 1920px;
    margin: 0 auto;
  }

  .ylarivi-ryhma {
    display: flex;
    align-items: center;
    gap: 15px;
  }

  .haku-ryhma {
    flex: 1;
    min-width: 0;
  }

  .oikea-puoli {
    display: flex;
    align-items: center;
    gap: 20px;
  }

  @media screen and (min-width: 1400px) {
    .ylarivin-sisalto {
      padding: 25px 15vw;
      gap: 40px;
    }
  }

  @media screen and (max-width: 1400px) {
    .ylarivin-sisalto {
      padding: 20px 10vw;
      gap: 25px;
    }
  }

  @media screen and (max-width: 1200px) {
    .ylarivin-sisalto {
      padding: 15px 5vw;
      gap: 20px;
    }
  }

  @media screen and (max-width: 900px) {
    .ylarivin-sisalto {
      padding: 15px 2vw;
      gap: 15px;
    }
  }

  @media screen and (max-width: 390px) {
    .ylarivin-sisalto {
      flex-direction: column;
      padding: 8px 10px;
      gap: 12px;
    }

    .ylarivi-ryhma {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 15px;
      width: 100%;
    }

    .haku-ryhma {
      width: 100%;
      max-width: none;
    }

    .oikea-puoli {
      flex-direction: column;
      width: 100%;
      gap: 12px;
    }
  }
</style>
