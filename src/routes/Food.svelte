<script>
  import Slide from "../lib/Slide.svelte";
  import Banner from "../lib/Banner.svelte";
  import Card from "../lib/Card.svelte";

  import { slideImages } from "../data/foodSlide";
  import { landingImages } from "../data/foodLanding";
</script>

<Slide images={slideImages}/>
<Banner title="Food" />

<main class="h-3/5 sm:h-screen">
  <div class="container mx-auto overflow-y-scroll sm:overflow-y-visible h-full">
    {#each landingImages as img}
      <Card url={img} />
    {/each}
  </div>
</main>

<main>
</main>

<style>
</style>
