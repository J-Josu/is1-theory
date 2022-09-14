<script lang="ts">
  import Assigment from './Assigment.svelte';
  import Objective from './Objective.svelte';
  import Question from './Question.svelte';
  export let startTime: number[];
  type Item = {
    type: string;
    time: number[];
    title?: string;
    items?: string[];
    index?: number;
    question?: string;
    tracing?: string;
  };
  export let items: Item[];
  let summary: {
    questiosnObjetivesTime: number[];
    questionsTracingTime: number[];
    totalTime: number[];
  };
  let endTime: string;
</script>

<div class="container">
  <div class="grid">
    <p>Tiempo asignado (minutos)</p>
    <p>Pregunta u objetivo del administrador</p>
    <p>Respuesta del entrevistado</p>
  </div>
  {#each items as item}
    <Assigment time={item.time}>
      {#if item.type === 'objetive'}
        <Objective category={item.title} objectives={item.items} />
      {:else}
        <Question
          index={item.index}
          question={item.question}
          tracing={item.tracing}
        />
      {/if}
    </Assigment>
  {/each}
  {#if summary}
    <Assigment time={summary.questiosnObjetivesTime}>
      <p>Tiempo asignado para preguntas y objetivos</p>
    </Assigment>
    <Assigment time={summary.questionsTracingTime}>
      <p>Tiempo asignado para preguntas de seguimiento y redireccion</p>
    </Assigment>
    <Assigment time={summary.totalTime}>
      <p>Tiempo asignado para la entrevista ({startTime} a {endTime})</p>
    </Assigment>
  {/if}
</div>

<style>
  .container {
    padding: 0rem;
  }
  :global(.grid) {
    display: grid;
    grid-template-columns: 80px 1fr 1fr;
  }
  :global(.grid > *) {
    border: 1px solid lightgrey;
    padding: 0.15rem;
  }
  @media screen and (min-width: 688px) {
    .container {
      padding: 1rem;
    }
    :global(.grid > *) {
      padding: 0.25rem;
    }
  }
</style>
