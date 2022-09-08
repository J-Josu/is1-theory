<script lang="ts">
  export let name: string;
  export let content: string;
</script>

<div class="container">
  <p><b>{name}:</b> {content}</p>
</div>

<style>
  .container {
    padding-block: 0.5rem;
  }
  p {
    font-size: 1.1rem;
  }
  p::first-letter {
    text-transform: uppercase;
  }
</style>
