<script>
  import Brandit from "./brandit.svelte";

  let brandit1 = [
    { nimi: "APNX", url: "#" },
    { nimi: "Ducky", url: "#" },
    { nimi: "Endgame Gear", url: "#" },
    { nimi: "HAVN", url: "#" },
    { nimi: "Kolink", url: "#" },
    { nimi: "Nitro Concepts", url: "#" },
    { nimi: "noblechairs", url: "#" },
    { nimi: "Streamplify", url: "#" },
    { nimi: "TRYX", url: "#" },
  ];

  let brandit2 = [
    { nimi: "Asus", url: "#" },
    { nimi: "Acer", url: "#" },
    { nimi: "Akasa", url: "#" },
    { nimi: "ASRock", url: "#" },
    { nimi: "Cooler Master", url: "#" },
    { nimi: "Corsair", url: "#" },
    { nimi: "Fractal Design", url: "#" },
    { nimi: "Gigabyte", url: "#" },
    { nimi: "Logitech", url: "#" },
    { nimi: "Phanteks", url: "#" },
  ];
</script>

<div class="list-container">
  <Brandit brandit={brandit1} />
</div>
<div class="list-container">
  <Brandit brandit={brandit2} />
</div>

<style>
  .list-container {
    margin-bottom: 20px; /* Creates a gap between the two lists */
  }
</style>
