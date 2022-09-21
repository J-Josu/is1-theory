<script lang="ts">
  export let index: number;
  export let question: string;
  export let tracing: {
    title: string;
    items: string[];
  }[];
  export let objective: string;
</script>

<div>
  <h5>Pregunta {index + 1}</h5>
  <p>{question}</p>
  <h5>{tracing.length > 0 ? 'Seguimiento' : ''}</h5>
  {#each tracing as { title, items }}
    <p>{title}</p>
    <ul>
      {#each items as sentence}
        <li>{sentence}</li>
      {/each}
    </ul>
  {/each}
  {#if objective}
    <h5>Objetivo</h5>
    <p>{objective}</p>
  {/if}
</div>

<style>
  h5 {
    font-size: 1rem;
    font-weight: 500;
  }
  div > h5:not(:first-child) {
    margin-top: 0.125rem;
  }
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
