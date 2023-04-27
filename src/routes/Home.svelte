<script>
  import Slide from "../lib/Slide.svelte";
  import Banner from "../lib/Banner.svelte";
  import Card from "../lib/Card.svelte";
  import img from "../assets/img.jpeg";

  import { images } from "../data/home";

</script>

<Slide {images}/>
<Banner title="Take a Tour" />

<main class="h-3/5 sm:h-screen pt-4">
  <div class="container mx-auto overflow-y-scroll sm:overflow-y-visible h-full">
    <Card {img} />
    <Card {img} />
    <Card {img} />
    <Card {img} />
  </div>
</main>

<style>
  @media (max-width: 640px) {
    ::-webkit-scrollbar {
      width: 10px;
    }
    ::-webkit-scrollbar-track {
      background: #f1f1f1;
      border-radius: 10px;
    }
    ::-webkit-scrollbar-thumb {
      background: lightgray;
      border-radius: 10px;
    }
    ::-webkit-scrollbar-thumb:hover {
      background: #555;
    }
  }
</style>
