<script>
  import Vuosi from "./vuosi.svelte";
  import EhdotJaSelosteet from "./ehdot-ja-selosteet.svelte";
</script>

<div class="virallinen-osio">
  <EhdotJaSelosteet />
  <Vuosi />
</div>

<style>
  .virallinen-osio {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px 0;
    background-color: #1a1d20;
    gap: 10px;
  }

  .virallinen-osio > :not(:last-child) {
    margin-bottom: 10px;
  }
</style>
