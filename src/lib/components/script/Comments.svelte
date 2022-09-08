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
  ul {
    margin-left: 1.5rem;
  }
  li {
    list-style: circle;
  }
</style>
