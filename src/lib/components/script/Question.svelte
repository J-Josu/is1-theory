<script lang="ts">
  export let index: number = 0;
  export let question: string = '';
  export let tracing: {
    then?: string[];
    otherwise?: string[];
  };
</script>

<div>
  <h5>Pregunta {index + 1}</h5>
  <p>{question}</p>
  <h5>{tracing.then || tracing.otherwise ? 'Seguimiento' : ''}</h5>
  {#if tracing.then}
    <p>Si es asi:</p>
    <ul>
      {#each tracing.then as otherQuestion}
        <li>{otherQuestion}</li>
      {/each}
    </ul>
  {/if}
  {#if tracing.otherwise}
    <p>Sino es asi:</p>
    <ul>
      {#each tracing.otherwise as otherQuestion}
        <li>{otherQuestion}</li>
      {/each}
    </ul>
  {/if}
</div>

<style>
  p {
    margin-left: 0.25rem;
    padding-block: 0.25rem;
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
