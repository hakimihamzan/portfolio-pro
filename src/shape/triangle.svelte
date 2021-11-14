<script>
  let randomColor = Math.floor(Math.random() * 16777215).toString(16);
  let arrowId = document.getElementById("arrow-down");

  function changeColor() {
    randomColor = Math.floor(Math.random() * 16777215).toString(16);
    arrowId.style.borderTop = `200px solid #${randomColor}`;
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
