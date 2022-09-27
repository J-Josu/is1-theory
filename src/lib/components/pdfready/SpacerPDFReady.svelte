<script lang="ts">
  import { pdfReady } from '$lib/store';
  export let height: string;
</script>

{#if $pdfReady}
  <div style:height />
{/if}
