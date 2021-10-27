<script>
  import ContactForm from "./ContactForm.svelte";
  function w3_close() {
    document.getElementById("mySidebar").style.display = "none";
  }
</script>

<!-- Sidebar -->
<div
  class="w3-sidebar w3-bar-block w3-border-right"
  style="display:none"
  id="mySidebar"
>
  <button on:click={w3_close} class="w3-bar-item w3-large w3-center"
    >Close &times;</button
  >
  <div class="w3-display-container w3-center">
    <!-- <img
      class="w3-circle"
      src="https://dilangunes.netlify.app/assets/img/dilan-pp.jpg"
      style="width:15rem"
      alt="Avatar"
    /> -->

    <h2
      class="w3-center"
      style="font-family: 'Ephesis', cursive; font-weight: bold; font-size:3rem"
    >
      Dilan Güneş
    </h2>
    <!-- <p class="w3-center">Researcher / PhD. Candidate</p> -->
  </div>
  <div class="w3-container w3-center">
    <i class="fa fa-facebook-official w3-hover-opacity w3-i" />
    <i class="fa fa-instagram w3-hover-opacity w3-i" />
    <i class="fa fa-snapchat w3-hover-opacity w3-i" />
    <br />
  </div>
  <a href="#about" class="w3-bar-item w3-button">Link 1</a>
  <a href="#publication" class="w3-bar-item w3-button">Link 2</a>
  <a href="#phd" class="w3-bar-item w3-button">Link 3</a>

  <ContactForm />
</div>

<style>
  .w3-i {
    font-size: 1.75rem;
    color: blueviolet;
  }

  .w3-i:hover {
    color: red;
  }
</style>
