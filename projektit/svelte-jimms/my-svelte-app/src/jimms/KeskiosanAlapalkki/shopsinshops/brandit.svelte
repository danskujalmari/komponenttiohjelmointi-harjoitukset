<script>
  import Brandi from "./brandi.svelte";
  let { brandit } = $props();
</script>

<ul class="brandit">
  {#each brandit as brandi}
    <li>
      <Brandi nimi={brandi.nimi} url={brandi.url} />
    </li>
  {/each}
</ul>

<style>
  .brandit {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
  }

  .brandit li {
    display: flex;
    text-decoration: none;
    border-right: 1px solid var(--väri-teksti);
    padding: 0 8px;
  }

  .brandit li:last-child {
    border-right: none;
  }
</style>
