<script>
  import Slide from "../lib/Slide.svelte";
  import Banner from "../lib/Banner.svelte";
  import Card from "../lib/Card.svelte";

  import { slideImages } from "../data/foodSlide";
  import { landingImages } from "../data/foodLanding";
  import Content from "../lib/Content.svelte";
</script>

<Slide images={slideImages}/>
<Banner title="Food" />

<Content>
  {#each landingImages as img}
    <Card url={img} />
  {/each}
</Content>
