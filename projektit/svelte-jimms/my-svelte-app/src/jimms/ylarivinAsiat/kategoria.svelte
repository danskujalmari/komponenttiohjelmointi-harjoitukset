<script>
  export let nimi;
  export let url;
</script>

<div>
  <a href={url}>{nimi}</a>
</div>

<style>
  a:any-link {
    padding: 10px 5px;
    text-decoration: none;
    color: var(--väri-teksti);
  }

  a:hover {
    background-color: var(--väri-teksti);
    color: var(--väri-linkki-tausta-hover);
  }
</style>
