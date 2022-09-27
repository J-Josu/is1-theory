<script lang="ts">
  import { pdfReady } from '$lib/store';
</script>

<div>
  <button class:printing={$pdfReady} on:click={() => ($pdfReady = !$pdfReady)}
    >Preparar<br />para pdf</button
  >
</div>

<style>
  div {
    position: fixed;
    bottom: 0;
    right: 0;
  }
  button {
    margin: 1ch;
    padding: 1ch;
    background: none;
    border: 1px solid lightgray;
    font-size: 0.75rem;
    opacity: 0.5;
  }
  button.printing {
    opacity: 0;
  }
  button:hover {
    opacity: 1;
  }
</style>
