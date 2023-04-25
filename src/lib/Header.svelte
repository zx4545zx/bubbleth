<script>
  import { Link } from "svelte-routing";

  import highlight from "../assets/icon/highlight.png";
  import food from "../assets/icon/food.png";
  import review from "../assets/icon/review.png";
  import event from "../assets/icon/event.png";
</script>

<div class="flex items-center justify-between px-16 py-6">
  <Link to="highlight">
    <img src={highlight} alt="highlight-icon" class="w-24" />
  </Link>
  <Link to="food">
    <img src={food} alt="food-icon" class="w-24" />
  </Link>
  <Link to="review">
    <img src={review} alt="review-icon" class="w-24" />
  </Link>
  <Link to="event">
    <img src={event} alt="event-icon" class="w-24" />
  </Link>
</div>
