<script>
  export let url = '#';
  export let nimi = 'Ehto tai seloste';
</script>

<div class="ehto-tai-seloste">
  <a href={url} target="_blank" rel="noopener noreferrer">{nimi}</a>
</div>

<style>
  .ehto-tai-seloste a {
    color: var(--väri-teksti);
    text-decoration: none;
  }

  .ehto-tai-seloste a:hover {
    color: var(--väri-linkki-tausta-hover);
  }
</style>
