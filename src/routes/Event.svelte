<script>
  import Slide from "../lib/Slide.svelte";
  import Banner from "../lib/Banner.svelte";
  import Content from "../lib/Content.svelte";
  import Card from "../lib/Card.svelte";

  import { slideImages } from "../data/eventSlide";
  import { landingImages } from "../data/eventLanding";
</script>

<Slide images={slideImages} />
<Banner title="Event" />

<Content>
  {#each landingImages as img}
    <Card url={img.url} title={img.title} des={img.des} />
  {/each}
</Content>

<style>
</style>
