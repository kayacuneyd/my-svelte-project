<script>
  import ContactForm from "./ContactForm.svelte";
  import Social from "./Social.svelte";

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
  <Social />
  <a href="#about" class="w3-bar-item w3-button">Link 1</a>
  <a href="#publication" class="w3-bar-item w3-button">Link 2</a>
  <a href="#phd" class="w3-bar-item w3-button">Link 3</a>

  <ContactForm />
</div>
