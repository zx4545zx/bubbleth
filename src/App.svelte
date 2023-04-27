<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import About from "./routes/About.svelte";
  import Highlight from "./routes/Highlight.svelte";
  import Food from "./routes/Food.svelte";
  import Review from "./routes/Review.svelte";
  import Event from "./routes/Event.svelte";

  import Navbar from "./lib/layout/Navbar.svelte";
  import Header from "./lib/Header.svelte";

  import highlight from "./assets/icon/highlight.png";
  import food from "./assets/icon/food.png";
  import review from "./assets/icon/review.png";
  import event from "./assets/icon/event.png";

  export let url = "";
</script>

<main class="h-screen md:h-auto overflow-hidden sm:overflow-visible">
  <Router {url}>
    <div class="container mx-auto">
      <Navbar />
      <Header />
    </div>
    <div class="container mx-auto">
      <Route path="event" component={Event} />
      <Route path="review" component={Review} />
      <Route path="food" component={Food} />
      <Route path="highlight" component={Home} />
      <Route path="about" component={About} />
      <Route path="/"><Home /></Route>
    </div>

    <div class="b-nav fixed sm:hidden w-full px-3 bg-black bottom-0">
      <ul class="flex justify-center items-center gap-8 p-2" style="margin-top: -1rem;">
        <li class="hover:text-slate-900">
          <Link to="highlight">
            <img src={highlight} alt="highlight-icon" class="w-16" />
          </Link>
        </li>
        <li class="hover:text-slate-900">
          <Link to="food">
            <img src={food} alt="food-icon" class="w-16" />
          </Link>
        </li>
        <li class="hover:text-slate-900">
          <Link to="review">
            <img src={review} alt="review-icon" class="w-16" />
          </Link>
        </li>
        <li class="hover:text-slate-900">
          <Link to="event">
            <img src={event} alt="event-icon" class="w-16" />
          </Link>
        </li>
      </ul>
    </div>
  </Router>
</main>

<style>
  .b-nav {
    background-image: url("./assets/bg-nav.jpeg");
    background-repeat: no-repeat;
    background-size: cover;
  }
  main {
    background-image: url("./assets/bg-xl.jpeg");
    background-repeat: no-repeat;
    background-size: cover;
  }
  @media (max-width: 425px) {
    main {
      background-image: url("./assets/bg-sm.jpeg");
      background-repeat: no-repeat;
      background-size: cover;
    }
  }
</style>
