<script lang="ts">
  export let time: number[];
  export let answer: string = '';
</script>

<div class="grid">
  <p style:text-align="center">{time?.map((n) => n.toString()).join(' - ')}</p>
  <slot />
  <p>{answer}</p>
</div>

<style>
  div > :global(*) {
    padding-top: 0.25rem;
  }
</style>
