<script lang="ts">
  export let time: string;
  export let answer: string = '';
</script>

<div class="grid">
  <p>{time} min.</p>
  <slot />
  <p>{answer}</p>
</div>

<style>
</style>
