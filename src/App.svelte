<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import About from "./routes/About.svelte";
  import Highlight from "./routes/Highlight.svelte";
  import Food from "./routes/Food.svelte";
  import Review from "./routes/Review.svelte";
  import Event from "./routes/Event.svelte";

  import Navbar from "./lib/layout/Navbar.svelte";
  import Slide from "./lib/Slide.svelte";
  import Banner from "./lib/Banner.svelte";
  import Header from "./lib/Header.svelte";

  export let url = "";
</script>

<main>
  <Router {url}>
    <div class="container mx-auto">
      <Navbar />
      <Header />
      <Slide />
      <Banner title="home" />
    </div>
    <div class="container mx-auto h-screen">
      <Route path="event" component={Event} />
      <Route path="review" component={Review} />
      <Route path="food" component={Food} />
      <Route path="highlight" component={Highlight} />
      <Route path="about" component={About} />
      <Route path="/"><Home /></Route>
    </div>
  </Router>
</main>

<style>
  main {
    background-image: url("./assets/bg-xl.jpeg");
    background-repeat: no-repeat;
    background-size: cover;
  }
</style>
