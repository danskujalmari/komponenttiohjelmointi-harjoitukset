<script>
  import Mustabaari from "./mustabaari.svelte";
  import SearchSection from "./searchsection.svelte";
  import Selitykset from "./selitykset.svelte";
</script>

<div class="sisalto">
  <Mustabaari />
  <SearchSection />
  <Selitykset />
</div>

<style>
  @media (max-width: 390px) {
    .sisalto {
      width: 100%;
      padding: 0;
    }
  }
</style>
