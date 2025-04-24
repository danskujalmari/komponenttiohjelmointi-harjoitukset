<script>
  import EhtoTaiSeloste from "./ehto-tai-seloste.svelte";

  let ehdot_ja_selosteet = [
    { nimi: "Takuu- ja toimitusehdot", url: "/takuujatoimitus" },
    { nimi: "Tietosuojaseloste", url: "/tietosuojaseloste" },
  ];
</script>

<ul class="ehdot-ja-selosteet">
  {#each ehdot_ja_selosteet as alkio}
    <li>
      <EhtoTaiSeloste {...alkio} />
    </li>
  {/each}
</ul>

<style>
  .ehdot-ja-selosteet {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    justify-content: center;
    font-size: 0.9rem;
    gap: 12px;
  }

  .ehdot-ja-selosteet li {
    display: inline;
  }
</style>
