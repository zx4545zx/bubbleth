<script>
  import { Splide, SplideSlide } from "@splidejs/svelte-splide";
  import frame from "../assets/frame.png";
  import defaultImg from "../assets/home/slide/0.jpg";

  let options = {
    width: "100%",
    gap: "1rem",
    type: "loop",
    autoplay: true,
    perPage: 1,
    pagination: false,
    speed: 1000,
  };

  export let images = [defaultImg];
</script>

<div class="container m-auto">
  <Splide {options}>
    {#each images as img}
      <SplideSlide>
        <div class="relative">
          <div class="relative">
            <div
              class="absolute top-4 sm:top-1 left-0 w-full h-full"
              style="z-index: -1;"
            >
              <img
                src={img}
                alt="slimg"
                class="slide-img mt-6 sm:mt-9 lg:mt-16 mx-auto h-4/6"
              />
            </div>
            <img src={frame} alt="frame-img" class="frame-img mx-auto" />
          </div>
        </div>
      </SplideSlide>
    {/each}
  </Splide>
</div>

<style>
  .slide-img {
    width: 80%;
    max-width: 65rem;
    object-fit: cover;
    object-position: center;
    overflow: hidden;
  }
  @media (max-width: 500px) {
    .slide-img {
      margin-top: 1rem;
    }
  }
  @media (max-width: 425px) {
    .frame-img {
      height: 14rem;
    }
  }
  @media (max-width: 300px) {
    .slide-img {
      margin-top: 0.5rem;
    }
  }
</style>
