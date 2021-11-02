<script>
  import { onMount } from "svelte";

  const apiURL = "./assets/js/data.json";
  let data = [];

  onMount(async () => {
    const response = await fetch(apiURL);
    data = await response.json();
  });

  function myFunction() {
    let x = document.getElementById("demo");
    if (x.className.indexOf("w3-show") == -1) {
      x.className += " w3-show";
    } else {
      x.className = x.className.replace(" w3-show", "");
    }
  }
</script>

<div class="w3-bar w3-gray">
  <a href="/" class="w3-bar-item w3-button">HOME</a>
  {#each data as item}
    <a href="#{item.id}" class="w3-bar-item w3-button w3-hide-small"
      >{item.id.toUpperCase()}</a
    >
  {/each}

  <a
    class="w3-bar-item w3-button w3-right w3-hide-large w3-hide-medium"
    on:click={myFunction}>&#9776;</a
  >
</div>

<div id="demo" class="w3-bar-block w3-red w3-hide w3-hide-large w3-hide-medium">
  <a href="/" class="w3-bar-item w3-button">HOME</a>
  {#each data as item}
    <a href="#{item.id}" class="w3-bar-item w3-button"
      >{item.id.toUpperCase()}</a
    >
  {/each}
</div>
