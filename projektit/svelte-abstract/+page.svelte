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
  @media (max-width: 375px) {
  }

  @media (max-width: 768px) {
    .sisalto {
      width: 140vw;
      max-width: 131.5vw;
    }
  }

  @media (max-width: 1200px) {
    .sisalto {
      min-width: 30vw;
    }
  }
</style>
