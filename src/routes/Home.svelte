<script>
  import Slide from "../lib/Slide.svelte";
  import Banner from "../lib/Banner.svelte";
  import Card from "../lib/Card.svelte";

  import img from "../assets/img.jpeg";
</script>

<Slide />
<Banner title="Home" />

<main class="h-80 sm:h-screen pt-4">
  <div class="container mx-auto overflow-scroll sm:overflow-visible h-full">
    <Card {img} />
    <Card {img} />
    <Card {img} />
    <Card {img} />
  </div>
</main>

<style>
  @media (max-width: 640px) {
    ::-webkit-scrollbar {
      -webkit-appearance: none;
      width: 7px;
    }

    ::-webkit-scrollbar-thumb {
      border-radius: 4px;
      background-color: rgba(0, 0, 0, 0.5);
      box-shadow: 0 0 1px rgba(255, 255, 255, 0.5);
    }
  }
</style>
