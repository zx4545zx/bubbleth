<script>
  import { Router, Link, Route } from "svelte-routing";
  import Home from "./routes/Home.svelte";
  import About from "./routes/About.svelte";

  import Navbar from "./lib/layout/Navbar.svelte";

  export let url = "";
</script>

<Router url="{url}">
  <Navbar/>
  <div>
    <Route path="about" component="{About}" />
    <Route path="/"><Home /></Route>
  </div>
</Router>

<style>

</style>
