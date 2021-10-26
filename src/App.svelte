<script>
  import LeftColumn from "./LeftColumn.svelte";
  import RightColumn from "./RightColumn.svelte";
</script>

<!-- Page Container -->
<div class="w3-content" style="max-width:1400px;">
  <!-- <img
    class="w3-image"
    src="https://www.w3schools.com/w3css/img_snowtops.jpg"
    alt="Norway"
    style="width:100%"
  /> -->
  <!-- The Grid -->
  <div class="w3-row">
    <LeftColumn />

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
</style>
