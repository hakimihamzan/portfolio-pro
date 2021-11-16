<script>
  let randomColor = Math.floor(Math.random() * 16777215).toString(16);
  let countToStick = 0;

  function changeColor() {
    let arrowId = document.getElementById("arrow-down");
    countToStick += 1;
    randomColor = Math.floor(Math.random() * 16777215).toString(16);
    arrowId.style.borderTop = `200px solid #${randomColor}`;

    if (countToStick > 20) {
      arrowId.style.transform = "rotate(75deg)";
      arrowId.style.borderLeft = "200px solid transparent";
      arrowId.style.borderRight = "200px solid transparent";
      arrowId.style.borderTop = "200px solid transparent";
    } else if (countToStick > 4) {
      console.log(countToStick);
      arrowId.style.transform = "rotate(0deg)";
      arrowId.style.borderLeft = "250px solid transparent";
      arrowId.style.borderRight = "250px solid transparent";
      arrowId.style.borderTop = "250px solid transparent";
    }
  }
</script>

<main>
  <div id="arrow-down" on:click={changeColor} class="arrow-down" style="border-top: 200px solid #{randomColor};" />
</main>

<style>
  .arrow-down {
    position: absolute;
    left: -250px;
    width: 0;
    height: 0;
    border-left: 200px solid transparent;
    border-right: 200px solid transparent;
    border-top: 200px solid transparent;
    transform: rotate(75deg);
    cursor: pointer;
    transition: 0.5s;
  }
  .arrow-down:hover {
    border-left: 250px solid transparent;
    border-right: 250px solid transparent;
    border-top: 250px solid transparent;
    transform: rotate(-10deg);
  }
</style>
