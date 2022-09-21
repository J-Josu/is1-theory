<script lang="ts">
  export let comments: string[];
</script>

<div>
  <h5>Comentarios generales y notas:</h5>
  <ul>
    {#each comments as comment}
      <li>{comment}</li>
    {/each}
  </ul>
</div>

<style>
  div {
    padding: 1rem;
  }
  h5 {
    font-size: 1rem;
    font-weight: 500;
  }
  ul {
    margin-left: 0.5rem;
    margin-top: 0.25rem;
  }
  li {
    margin-left: 0.5rem;
    padding-left: 0.5rem;
  }
  li::marker {
    content: '-';
    margin-left: 0.25rem;
  }
</style>
