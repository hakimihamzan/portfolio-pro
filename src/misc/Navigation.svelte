<script>
  // let controller = (e) => {
  //   e.preventDefault();
  //   switch (e.target.hash) {
  //     case "#home":
  //       {
  //         window.location.hash = "#home";
  //       }
  //       break;
  //     case "#portfolio":
  //       {
  //         window.location.hash = "#portfolio";
  //       }
  //       break;
  //     case "#contact":
  //       {
  //         window.location.hash = "#contact";
  //       }
  //       break;
  //     case "#about":
  //       {
  //         window.location.hash = "#about";
  //       }
  //       break;
  //   }
  // };
</script>

<main>
  <div class="outer">
    <a href="#home">Home</a>
    <div class="m-5">|</div>
    <a href="#portfolio">Portfolio</a>
    <div class="m-5">|</div>
    <a href="#contact">Contact</a>
    <div class="m-5">|</div>
    <a href="#about">About</a>
  </div>
</main>

<style>
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
    margin: 0 25px;
    font-size: 2rem;
  }
</style>
