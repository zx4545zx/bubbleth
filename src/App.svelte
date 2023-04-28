<script>
  import { Router, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import About from "./routes/About.svelte";
  import Food from "./routes/Food.svelte";
  import Review from "./routes/Review.svelte";
  import Event from "./routes/Event.svelte";

  import Navbar from "./lib/layout/Navbar.svelte";
  import Header from "./lib/Header.svelte";
  import Footer from "./lib/layout/Footer.svelte";
  import BottomNavbar from "./lib/layout/BottomNavbar.svelte";

  export let url = "";
</script>

<main class="w-100 overflow-x-hidden">
  <Router {url}>
    <div class="container mx-auto">
      <Navbar />
      <Header />
    </div>
    <div class="container mx-auto h-4/5 sm:h-auto">
      <Route path="event" component={Event} />
      <Route path="review" component={Review} />
      <Route path="food" component={Food} />
      <Route path="highlight" component={Home} />
      <Route path="about" component={About} />
      <Route path="/" component={Home}></Route>
    </div>
    <Footer />
    <BottomNavbar />
  </Router>
</main>

<style>
  /* main {
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
  } */
</style>
