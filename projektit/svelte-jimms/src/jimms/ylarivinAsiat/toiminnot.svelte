<script>
  import Kirjautuminen from "./kirjautuminen.svelte";
  import Ostoskori from "./ostoskori.svelte";
</script>

<div class="toiminnot">
  <Kirjautuminen />
  <Ostoskori />
</div>

<style>
  .toiminnot {
    display: flex;
    gap: 15px;
    align-items: center;
  }
</style>
