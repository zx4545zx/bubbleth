<script>
  import { Link } from "svelte-routing";
  import logo from "../../assets/logo.png";
</script>

<div class="navbar bg-transparent px-4 justify-center">
  <div class="navbar-start hidden sm:flex">
    <Link class="normal-case text-xl" to="/" alt="logo">
      <div class="avatar">
        <div class="w-20 rounded-full">
          <img src={logo} alt="logo">  
        </div>
      </div>
    </Link>
  </div>
  <div class="navbar-center sm:hidden">
    <div class="avatar">
        <div class="w-20 rounded-full">
          <img src={logo} alt="logo">  
        </div>
      </div>
  </div>
  <div class="navbar-end hidden sm:flex">
    <ul class="flex justify-center items-center gap-8 text-black">
      <li><Link to="highlight">Highlight</Link></li>
      <li><Link to="food">Food</Link></li>
      <li><Link to="review">Review</Link></li>
      <li><Link to="event">Event</Link></li>
      <li><Link to="about">About</Link></li>
    </ul>
  </div>
</div>

<style>
  .navbar-center ul li:hover {
    border-bottom: 4px solid lightseagreen;
  }
</style>