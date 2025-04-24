<script>
  import Artikkelitjablogi from "./artikkelitjablogi.svelte";
  import Info from "./info.svelte";
  import Sertifikaatitjapalkinnot from "./sertifikaatitjapalkinnot.svelte";
  import ShopInShopsSisalto from "./shopsinshops/shop-in-shops.svelte";
</script>

<div class="sisalto">
  <Info />
  <section class="shops-in-shops">
    <h2>shops-in-shops</h2>
    <ShopInShopsSisalto />
  </section>
  <Artikkelitjablogi />
  <Sertifikaatitjapalkinnot />
</div>

<style>
  .sisalto {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 1vw 15vw;
    gap: 20px;
  }

  .shops-in-shops {
    width: 400px;
  }

  .shops-in-shops h2 {
    padding-left: 8px;
    margin-bottom: 15px;
    color: #fff;
    text-transform: uppercase;
    text-align: left;
  }

  @media screen and (max-width: 1400px) {
    .sisalto {
      padding: 1vw 10vw;
    }
  }

  @media screen and (max-width: 1200px) {
    .sisalto {
      padding: 1vw 5vw;
      flex-wrap: wrap;
      justify-content: space-around;
    }

    .shops-in-shops {
      width: 45%;
      min-width: 300px;
    }
  }

  @media screen and (max-width: 900px) {
    .sisalto {
      padding: 1vw 2vw;
    }
  }

  @media screen and (max-width: 680px) {
    .sisalto {
      flex-direction: column;
      padding: 20px 15px;
      gap: 25px;
    }

    .shops-in-shops {
      width: 100%;
      min-width: auto;
      padding: 0 10px;
      border-bottom: 1px solid #3f4144;
      padding-bottom: 20px;
    }

    :global(.sisalto > *) {
      width: 100%;
      padding: 0 10px;
      border-bottom: 1px solid #3f4144;
      padding-bottom: 20px;
    }

    :global(.sisalto > *:last-child) {
      border-bottom: none;
      padding-bottom: 0;
    }

    :global(.sisalto h2) {
      font-size: 18px;
      margin-bottom: 15px;
      color: #fff;
      text-transform: uppercase;
      text-align: left;
    }

    :global(.sisalto p) {
      margin: 8px 0;
      line-height: 1.4;
      text-align: left;
    }

    :global(.sisalto a) {
      display: block;
      padding: 8px 0;
      color: #fff;
      text-decoration: none;
      text-align: left;
    }
  }

  @media screen and (max-width: 390px) {
    .sisalto {
      padding: 15px 10px;
      gap: 20px;
    }

    .shops-in-shops {
      padding: 0 5px 15px 5px;
    }

    .shops-in-shops h2 {
      font-size: 16px;
      margin-bottom: 12px;
    }

    :global(.sisalto > *) {
      padding: 0 5px 15px 5px;
    }

    :global(.sisalto h2) {
      font-size: 16px;
      margin-bottom: 12px;
    }

    :global(.sisalto p) {
      font-size: 14px;
      margin: 6px 0;
    }

    :global(.sisalto a) {
      font-size: 14px;
      padding: 6px 0;
    }

    :global(.sisalto img) {
      max-width: 100%;
      height: auto;
      margin: 10px 0;
    }

    :global(.sisalto svg) {
      width: 16px;
      height: 16px;
      margin-right: 8px;
      vertical-align: middle;
    }
  }
</style>
