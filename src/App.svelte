<script>
  /* import { onMount } from "svelte"; */
  import Down from "./Down.svelte";
  import Footer from "./Footer.svelte";
  import Menu from "./Menu.svelte";

  /* const apiURL = "./assets/js/data.json";
  let data = [];

  onMount(async function () {
    const response = await fetch(apiURL);
    data = await response.json();
  }); */
</script>

<head:svelte>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Ephesis&display=swap"
    rel="stylesheet"
  />
</head:svelte>

<!-- Page Container -->
<div class="w3-container-full w3-footer-color">
  <!-- <button class="w3-button w3-teal w3-xlarge sidebar-button" on:click={w3_open}
    >☰</button
  > -->

  <div class="w3-top w3-shadow-light">
    <Menu />
  </div>

  <!-- The Grid -->
  <div class="w3-row w3-margin-top-15vh">
    <!-- Right Column -->

    <Down />
    <!-- {#each data as item}
      <div>
        <p>{item.subtitels}</p>
      </div>
    {/each} -->
    <!-- End Grid -->
  </div>

  <!-- End Page Container -->
</div>

<Footer />

<style>
  /* .sidebar-button {
    border-radius: 0 0 20px 0;
  } */
</style>
