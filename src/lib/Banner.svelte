<script>
  import banner from "../assets/banner.png";

  export let title = '';

</script>

<div class="m-auto p-0 sm:p-2 relative">
  <div class="absolute text-center w-full font-custom">{title}</div>
  <img src={banner} alt="banner" class="m-auto w-48 sm:w-auto max-w-xs">
</div>

<style>
  .font-custom {
    top: 35%;
    font-family: 'Pattaya', sans-serif;
  }
  @media (max-width: 640px) {
    .font-custom {
      top: 30%;
    }
  }
</style>
