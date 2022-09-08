<script lang="ts">
  export let category: string;
  export let objectives: string[];
</script>

<div>
  <h5>Objetivo</h5>
  <p>{category}</p>
  <ul>
    {#each objectives as objetive}
      <li>{objetive}</li>
    {/each}
  </ul>
</div>

<style>
  ul {
    margin-left: 1.5rem;
  }
  li {
    list-style: circle;
  }
</style>
