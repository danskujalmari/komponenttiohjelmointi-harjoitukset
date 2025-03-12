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
  @media (max-width: 375px) {
    .sisalto {
      width: 136.5vw;
    }
  }
</style>
