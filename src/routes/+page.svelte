<script>
  import {slide} from 'svelte/transition';

  let show = false;
  let items = [];
  for (let i = 0; i < 25; i++) {
    items.push(i);
  }
</script>

<h1>Welcome to SvelteKit</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>
<p><a href="other">Visit another page</a></p>

<input type="button" value="toggle" on:click={() => show = !show}>
<input type="button" value="insert" on:click={() => items = [...items, 'howdy']}>

{#if show}
  {#each items as item}
    <div transition:slide>
      {item}
    </div>
  {/each}
{/if}
