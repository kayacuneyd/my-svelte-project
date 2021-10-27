<script>
  import RightColumn from "./RightColumn.svelte";
  import Sidebar from "./Sidebar.svelte";

  function w3_open() {
    document.getElementById("mySidebar").style.display = "block";
  }
</script>

<head:svelte>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Ephesis&display=swap"
    rel="stylesheet"
  />
</head:svelte>

<!-- Sidebar -->
<Sidebar />

<!-- Page Container -->
<div class="w3-content">
  <button class="w3-button w3-teal w3-xlarge sidebar-button" on:click={w3_open}
    >☰</button
  >
  <!-- The Grid -->
  <div class="w3-row">
    <!-- Right Column -->
    <RightColumn />

    <!-- End Grid -->
  </div>

  <!-- End Page Container -->
</div>

<footer class="w3-container w3-grey w3-center">
  <p>Find me on social media.</p>
  <i class="fa fa-facebook-official w3-hover-opacity" />
  <i class="fa fa-instagram w3-hover-opacity" />
  <i class="fa fa-snapchat w3-hover-opacity" />
  <i class="fa fa-pinterest-p w3-hover-opacity" />
  <i class="fa fa-twitter w3-hover-opacity" />
  <i class="fa fa-linkedin w3-hover-opacity" />
  <p>
    Powered by <a
      href="https://www.w3schools.com/w3css/default.asp"
      target="_blank">w3.css</a
    >
  </p>
</footer>

<style>
  .sidebar-button {
    border-radius: 0 0 20px 0;
  }
</style>
