<script lang="ts">
  export let title: string = '';
  export let objectives: string[];
</script>

<div>
  <h5>{title}</h5>
  <ul>
    {#each objectives as objetive}
      <li>{objetive}</li>
    {/each}
  </ul>
</div>

<style>
  h5 {
    font-size: 1rem;
    font-weight: 500;
  }
  ul {
    margin-left: 0.25rem;
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
