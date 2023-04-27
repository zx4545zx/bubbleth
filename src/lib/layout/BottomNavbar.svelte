<script>
  import { Link } from "svelte-routing";
  import highlight from "../../assets/icon/highlight.png";
  import food from "../../assets/icon/food.png";
  import review from "../../assets/icon/review.png";
  import event from "../../assets/icon/event.png";
</script>

<div class="b-nav fixed block sm:hidden w-full px-3 bottom-0 h-[11%]">
  <ul class="flex justify-center items-center gap-8 p-2 -mt-1 h-full">
    <li>
      <Link to="highlight">
        <img src={highlight} alt="highlight-icon" class="w-16" />
      </Link>
    </li>
    <li>
      <Link to="food">
        <img src={food} alt="food-icon" class="w-16" />
      </Link>
    </li>
    <li>
      <Link to="review">
        <img src={review} alt="review-icon" class="w-16" />
      </Link>
    </li>
    <li>
      <Link to="event">
        <img src={event} alt="event-icon" class="w-16" />
      </Link>
    </li>
  </ul>
</div>

<style>
  * {
    font-family: "Pattaya", sans-serif;
  }
  .b-nav {
    background-image: url("../../assets/bg-nav.jpeg");
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>
