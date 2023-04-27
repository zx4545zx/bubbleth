<script>
  import Slide from "../lib/Slide.svelte";
  import Banner from "../lib/Banner.svelte";
  import Card from "../lib/Card.svelte";

  import { slideImages } from "../data/homeSlide";
  import { landingImages } from "../data/homeLanding";
</script>

<Slide images={slideImages} />
<Banner title="Take a Tour" />

<main class="h-3/5 sm:h-screen">
  <div class="container mx-auto overflow-y-scroll sm:overflow-y-visible h-full">
    {#each landingImages as img}
      <Card url={img.url} title={img.title} des={img.des} />
    {/each}
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
