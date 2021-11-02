<script>
  import { onMount } from "svelte";
  import ContactForm from "./ContactForm.svelte";
  import Up from "./Up.svelte";

  const apiURL = "./assets/js/data.json";
  let data = [];

  onMount(async () => {
    const response = await fetch(apiURL);
    data = await response.json();
  });

  function myFunction() {
    var x = document.getElementById("demo-3");
    if (x.className.indexOf("w3-show") == -1) {
      x.className += " w3-show";
    } else {
      x.className = x.className.replace(" w3-show", "");
    }
  }
  let subtitels = [
    "The Political Economy of Assassinations \n",

    "The Electoral Cycle of Violence \n",

    "The Effects of Female Mayors on Local Policy and Politics \n",

    "Criminal Dynamics and Homicides in Brazil \n",

    "Identifying and Deterring the Theft and Diversion of Medicinal Drugs in Malawi \n",
  ];
</script>

<div class="w3-center w3-margin">
  <Up />
  {#each data as item}
    <div class="w3-container w3-card w3-white w3-left-align w3-margin-bottom">
      <h2 class="w3-text-grey w3-padding-16">
        <i
          class="fa fa-question-circle fa-fw w3-margin-right w3-xxlarge w3-text-red"
        />{item.title}
      </h2>
      <div class="w3-container" id={item.id}>
        <h4 class="w3-opacity"><b>{item.id.toUpperCase()}</b></h4>
        <!-- <h6 class="w3-text-teal">
        <i class="fa fa-calendar fa-fw w3-margin-right" />Forever
      </h6> -->
        <p>{item.text}</p>
      </div>
      <!--Academic Papers-->
      {#if item.title !== "Research & Posts"}
        <br />
      {:else}
        <div class="w3-container">
          <ul class="w3-ul w3-hoverable">
            <li>
              <a href="/">The Electoral Cycle of Violence</a>
            </li>
            <li>
              <a href="/"
                >The Effects of Female Mayors on Local Policy and Politics</a
              >
            </li>
            <li><a href="/">Criminal Dynamics and Homicides in Brazil</a></li>
            <li><a href="/">Criminal Dynamics and Homicides in Brazil</a></li>
          </ul>
        </div>
      {/if}

      <!-- Academic Responsibilities -->
      {#if item.title !== "Academic Responsibilities"}
        <br />
      {:else}
        <div class="w3-container">
          <h5>The Title</h5>
          <p>{item.text}</p>
          <ul class="w3-ul">
            <li>IRGN 479: Program Design and Evaluation. UCSD, Winter 2016</li>
            <li>Statistics 1B. FGV, Spring 2015</li>
          </ul>
          <br />
          <h5>The Title</h5>
          <ul class="w3-ul">
            <li>
              POLI 11: Intro to Comparative Politics. Fall 2017, Summer 2021
            </li>
            <li>POLI 12: Intro to International Relations. Spring 2020</li>
            <li>POLI 30: Political Inquiry. Fall 2019</li>
            <li>INTL 102: World Poverty. Fall 2016</li>
            <li>
              POLI 199: Undergraduate research mentor. 2018-2019 and 2019-2020
              academic years
            </li>
          </ul>
        </div>
      {/if}
      <!-- CV -->
      {#if item.title !== "Curriculum Vitaes"}
        <br />
      {:else}
        <div class="w3-container">
          <p>
            {item.text} <a target="_blank" href="http://google.com">here</a>
          </p>
        </div>
      {/if}
    </div>
  {/each}

  <button
    on:click={myFunction}
    class="w3-btn w3-block w3-red w3-center"
    style="width:75%;margin-left: auto; margin-right: auto;"
  >
    You can contact with me via e-mail as well!</button
  >

  <div
    id="demo-3"
    class="w3-hide w3-container w3-center w3-pale-red"
    style="width:75%;margin-left: auto; margin-right: auto;"
  >
    <!-- <p>You can contact with me via e-mail as well!</p> -->
    <ContactForm />
  </div>

  <!-- End  -->
</div>
