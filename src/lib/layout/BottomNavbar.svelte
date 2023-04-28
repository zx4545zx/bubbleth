<script>
  import { Link } from "svelte-routing";
  import highlight from "../../assets/icon/highlight.png";
  import food from "../../assets/icon/food.png";
  import review from "../../assets/icon/review.png";
  import event from "../../assets/icon/event.png";

  import { navCount } from "../../store";

  let nav = [
    {
      to: "highlight",
      src: highlight
    },
    {
      to: "food",
      src: food
    },
    {
      to: "review",
      src: review
    },
    {
      to: "event",
      src: event
    }
  ];

</script>

<div class="b-nav fixed sm:hidden w-full px-3 bottom-0 h-[8%]">
  <ul class="flex justify-center items-center gap-8 p-2 h-full">
    {#each nav as n, i}
      <!-- svelte-ignore a11y-click-events-have-key-events -->
      <li class={$navCount == i && 'active -mt-8'} on:click={() => navCount.set(i)}>
        <Link to={n.to}>
          <img src={n.src} alt="highlight-icon" class={$navCount == i ? 'w-12' : "w-10"} />
        </Link>
      </li>
    {/each}
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
  .active {
    background-color: white;
    border-radius: 10px;
    padding: 4px;
    margin-bottom: 4px;
    box-shadow: 1px 1px 1px lightgray;
  }
</style>
