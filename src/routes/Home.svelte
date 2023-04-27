<script>
  import Slide from "../lib/Slide.svelte";
  import Banner from "../lib/Banner.svelte";
  import Card from "../lib/Card.svelte";

  import { slideImages } from "../data/homeSlide";
  import { landingImages } from "../data/homeLanding";
  import Content from "../lib/Content.svelte";
</script>

<Slide images={slideImages} />
<Banner title="Take a Tour" />

<Content>
  {#each landingImages as img}
    <Card url={img.url} title={img.title} des={img.des} />
  {/each}
</Content>