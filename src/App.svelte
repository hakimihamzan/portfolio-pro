<script>
  import About from "./about/About.svelte";
  import Contact from "./contact/Contact.svelte";
  import Home from "./home/Home.svelte";
  import Navigation from "./misc/Navigation.svelte";
  import Portfolio from "./portfolio/Portfolio.svelte";

  function clickMe() {
    console.log("clicked");
    document.querySelector(".home").style.transform = `translateX(-100vw)`;
    // document.querySelector(".porfolio").style.transform = `translateX(-200vw)`;
    // document.querySelector(".contact").style.transform = `translateX(-300vw)`;
    // document.querySelector(".about").style.transform = `translateX(-400vw)`;
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
    background: #d3cce3;
    background: -webkit-linear-gradient(to right, #e9e4f0, #d3cce3);
    background: linear-gradient(to right, #e9e4f0, #d3cce3);
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
