<script>
  import Title from "./home/Title.svelte";
  import Square from "./shape/Square.svelte";
  import Triangle from "./shape/Triangle.svelte";
  import Navigation from "./space/Navigation.svelte";
</script>

<main>
  <Triangle />
  <Title />
  <Square />
  <Navigation />
</main>

<style>
  main {
    margin: 0 auto;
  }
</style>
