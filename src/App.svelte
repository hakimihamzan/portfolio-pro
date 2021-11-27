<script>
  import About from "./about/About.svelte";
  import Contact from "./contact/Contact.svelte";
  import Home from "./home/Home.svelte";
  import Navigation from "./misc/Navigation.svelte";
  import Portfolio from "./portfolio/Portfolio.svelte";

  function removeClass() {
    let allTag = document.querySelectorAll(".aTag");
    allTag.forEach((eachNode, v) => eachNode.classList.remove("disLink"));
  }

  window.onhashchange = () => {
    switch (location.hash) {
      case "#home":
        {
          removeClass();
          document.querySelector(".aTag.Home").classList.add("disLink");
        }
        break;
      case "#portfolio":
        {
          removeClass();
          console.log("portfolio is active");
          document.querySelector(".aTag.Portfolio").classList.add("disLink");
        }
        break;
      case "#contact":
        {
          removeClass();
          console.log("contact is active");
          document.querySelector(".aTag.Contact").classList.add("disLink");
        }
        break;
      case "#about":
        {
          removeClass();
          console.log("about is active");
          document.querySelector(".aTag.About").classList.add("disLink");
        }
        break;
    }
  };

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

  // function clickMe() {
  //   document.querySelector(".home").style.transform = `translateX(-100vw)`;
  // }
</script>

<main>
  <div class="home"><Home /></div>
  <!-- <div class="porfolio"><Portfolio /></div>
  <div class="contact"><Contact /></div>
  <div class="about"><About /></div> -->
  <!-- <Navigation /> -->
  <!-- <button on:click={clickMe}>click</button> -->

  <!-- Bottom Navigation -->
  <div class="outer">
    <a href="#home" class="aTag Home disLink">Home</a>
    <div class="m-5">|</div>
    <a href="#portfolio" class="aTag Portfolio">Portfolio</a>
    <div class="m-5">|</div>
    <a href="#contact" class="aTag Contact">Contact</a>
    <div class="m-5">|</div>
    <a href="#about" class="aTag About">About</a>
  </div>
</main>

<style>
  main {
    width: 100vw;
    height: 100vh;
  }
  .home {
    transition: transform 1s;
  }
  .outer {
    position: absolute;
    width: 100vw;
    bottom: 10px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 1.3rem;
  }
  .m-5 {
    margin: 0 40px;
    font-size: 2rem;
  }
  .aTag {
    width: 100px;
  }
</style>
