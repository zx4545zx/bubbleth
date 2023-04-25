<script>
  import { Link } from "svelte-routing";
</script>

<nav>
  <div class="navbar bg-base-100">
    <div class="flex-1">
      <Link class="btn btn-ghost normal-case text-xl" to="/">daisyUI</Link>
    </div>
    <div class="flex-none">
      <ul class="menu menu-horizontal px-1">
        <li><Link to="/">Home</Link></li>
        <li><Link to="about">About</Link></li>
      </ul>
    </div>
  </div>
</nav>

<style>
  
</style>