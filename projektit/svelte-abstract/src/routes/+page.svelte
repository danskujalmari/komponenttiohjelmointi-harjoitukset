<script>
  import Ylapalkki from "../nettisivu/abstract/ylapalkki.svelte";
  import Font from "../nettisivu/abstract/global/globaalit-tyylit.svelte";
  import Alapalkki from "../nettisivu/abstract/alapalkki.svelte";
</script>

<div class="sisalto">
  <Ylapalkki />
  <Alapalkki />
  <Font />
</div>

<style>
  @media (max-width: 390px) {
    .sisalto {
      width: 100%;
      max-width: 100%;
    }
  }

  @media (max-width: 768px) {
    .sisalto {
      width: 100%;
      max-width: 100%;
    }
  }

  @media (max-width: 1200px) {
    .sisalto {
      width: 100%;
      max-width: 100%;
    }
  }
</style>
