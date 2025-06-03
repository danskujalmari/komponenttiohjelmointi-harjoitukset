<style>
  :global(:root) {
    font-family: "Open Sans", sans-serif;
    --väri-teksti: #dddddd;
    --väri-otsikot: #e9ecef;
    --väri-tausta-tumma: #272b30;
    --väri-tausta-tumma-toinen: #23272b;
    --väri-linkki-tausta-hover: #ee6622;
  }

  @font-face {
    font-family: "Open Sans";
    src: url("OpenSans-VariableFont_wdth,wght.ttf") format("truetype");
  }

  :global(ul) {
    padding: 0;
    margin: 0;
  }

  :global(li) {
    list-style: none;
  }

  :global(body) {
    margin: 0;
    padding: 0;
    background-color: var(--väri-tausta-tumma-toinen);
  }

  :global(h1, h2, h3, h4, h5, h6) {
    margin: 0;
    padding: 0;
    color: var(--väri-otsikot);
    text-transform: uppercase;
  }

  :global(svg) {
    width: 20px;
    height: 20px;
    fill: var(--väri-teksti);
  }

  @media (max-width: 680px) {
    :global(h1, h2, h3, h4, h5, h6) {
      color: var(--väri-otsikot);
      font-size: 1rem;
      text-align: center;
    }
  }
</style>
