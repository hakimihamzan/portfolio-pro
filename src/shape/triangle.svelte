<script>
  function changeColor() {
    let randomColor = Math.floor(Math.random() * 16777215).toString(16);

    console.log("hi", randomColor);
  }
</script>

<main>
  <div on:click={changeColor} class="arrow-down" />
</main>

<style>
  .arrow-down {
    position: absolute;
    left: -200px;
    width: 0;
    height: 0;
    border-left: 200px solid transparent;
    border-right: 200px solid transparent;
    border-top: 200px solid teal;
    transform: rotate(75deg);
  }
</style>
