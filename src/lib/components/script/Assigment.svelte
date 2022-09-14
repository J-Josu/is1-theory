<script lang="ts">
  export let time: number[];
  export let answer: string = '';
  
</script>

<div class="grid">
  <p>{time?.map(n => n.toString()).join(' a ')} min.</p>
  <slot />
  <p>{answer}</p>
</div>

<style>
</style>
