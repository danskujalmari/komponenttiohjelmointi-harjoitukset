<script>
  let { url, nimi } = $props();
</script>

<a href={url}>
  {nimi}
</a>

<style>
  a:link {
    color: var(--väri-teksti);
    text-decoration: none;
  }
  a:visited {
    color: var(--väri-teksti);
    text-decoration: none;
  }
  a:active {
    color: var(--väri-teksti);
    text-decoration: none;
  }
  a:hover {
    color: var(--väri-linkki-tausta-hover);
    text-decoration: none;
  }
</style>
