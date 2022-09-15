<script lang="ts">
  export let name: string;
  export let content: string;
</script>

<div class="container">
  <div class="inner">
    <h3>{name}:</h3>
    <span>{content}</span>
  </div>
  {#if $$slots.default}
    <div class="slot">
      <slot />
    </div>
  {/if}
</div>

<style>
  .container {
    padding-block: 1rem;
  }
  .inner {
    display: flex;
    margin-top: 1rem;
    font-size: 1.5rem;
    align-items: center;
  }
  h3 {
    font-size: 1.5rem;
    margin-right: 1ch;
  }
  h3::first-letter {
    text-transform: uppercase;
  }
  .slot {
    margin: 1rem 1rem 0 1rem;
  }
</style>
