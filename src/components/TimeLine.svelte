<script>
  import { onMount } from "svelte";
  import Card from "./Card.svelte";
  let data = [];
  let posts = []
  const API = "https://dog.ceo/api/breed/pug/images";
  onMount(async () => {
    const response = await fetch(API);
    data = await response.json();
    posts = data.message
  });
</script>

<div class="TimeLine">
  <div class="TimeLie-container">
    {#each posts as post }
        <Card image={post} />
        {:else}
        loading...
    {/each}
  </div>
</div>

<style>
  .TimeLine {
    padding: 4em 0 0 0;
  }
</style>
