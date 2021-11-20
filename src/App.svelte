<script>
  import About from "./about/About.svelte";
  import Contact from "./contact/Contact.svelte";
  import Home from "./home/Home.svelte";
  import Navigation from "./misc/Navigation.svelte";
  import Portfolio from "./portfolio/Portfolio.svelte";

  // ____________Home____________Portfolio____________Contact____________About______________
  // ____________Home_______________________________________________________________________
  // ____________________________Portfolio__________________________________________________
  // _________________________________________________Contact_______________________________
  // ____________________________________________________________________About______________
  // If home is active
  //        Portolio, Contact, About is inactive
  //        asdfjlksdjlkflkjl
  // If porfolio is active
  //        Contact, About, Home is inactive
  // If contact is active
  //        About, Home, Portfolio is inactive
  // If about is active
  //        Home, Portolio, Contact is inactive

  function clickMe() {
    document.querySelector(".home").style.transform = `translateX(-100vw)`;
  }
</script>

<main>
  <div class="home">
    <Home />
  </div>
  <div class="porfolio">
    <Portfolio />
  </div>
  <div class="contact">
    <Contact />
  </div>
  <div class="about">
    <About />
  </div>
  <Navigation />
  <button on:click={clickMe}>click</button>
</main>

<style>
  main {
    width: 100vw;
    height: 100vh;
  }
  .home {
    transition: transform 1s;
  }
  button {
    position: fixed;
    top: 0;
    left: 500px;
  }
</style>
