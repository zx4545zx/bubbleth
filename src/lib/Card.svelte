<script>
  import frame from "../assets/pic-frame.png";

  export let img;
</script>

<div class="relative w-full mt-8">
  <div class=" absolute w-full -mt-7 sm:-mt-12 lg:-mt-16 xl:-my-24">
    <img src={frame} alt="frame-img" class="m-auto w-full" />
  </div>
  <img
    src={img}
    alt="slimg"
    class="img-slide mx-auto w-5/6 
    sm:h-80 sm:ml-16 sm:w-[85%] 
    md:ml-20 md:h-96 
    lg:ml-28 lg:h-[33rem] 
    xl:h-[40rem] xl:ml-36 
    2xl:h-[48rem]"
  />
</div>
<div class="container pt-3 pb-16 px-12 text-center">
  <p class="p-4">อีเว้นท์มากมายที่น่าติดตาม</p>
  <span
    >อีเว้นท์ที่จะมีกิจกรรมสนุกๆ ให้ลูกค้าได้ร่วมสนุก
    อีกทั้งยังมีโปรโมชั่นอีกมากมายให้ติดตาม &nbsp;</span
  >
</div>

<style>
  * {
    font-family: 'Pattaya', sans-serif;
  }
  .img-slide {
    object-fit: cover;
  }
  @media (max-width: 640px) {
    .img-slide {
      margin-left: calc(100vw * 0.11);
      height: calc(100vw * 0.5);
      object-fit: cover;
    }
  }
</style>
