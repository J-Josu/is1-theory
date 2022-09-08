<script lang="ts">
  export let name: string;
  export let content: string;
</script>

<div class="container">
  <p><b>{name}:</b> {content}</p>
  {#if $$slots.default}
    <div>
      <slot />
    </div>
  {/if}
</div>

<style>
  .container {
    border-bottom: 2px solid gray;
    padding-block: 1rem;
  }
  p {
    margin-top: 1rem;
    font-size: 1.2rem;
  }
  p::first-letter {
    text-transform: uppercase;
  }
  .container > div {
    margin: 1rem 1rem 0 1rem;
  }
</style>
