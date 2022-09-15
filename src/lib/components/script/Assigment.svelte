<script lang="ts">
  export let time: number[];
  export let answer: string = '';
</script>

<div class="grid">
  {#if time.length === 1}
    <p style:text-align="center">{time[0]} min.</p>
  {:else}
    <p style:text-align="center">
      {time.map((n) => n.toString()).join(' a ')}<br />min.
    </p>
  {/if}
  <slot />
  <p>{answer}</p>
</div>

<style>
  div > :global(*) {
    padding-top: 0.25rem;
  }
</style>
