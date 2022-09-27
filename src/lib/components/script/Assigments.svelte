<script lang="ts">
  import SpacerPDFReady from '$cmps/pdfready/SpacerPDFReady.svelte';
  import Assigment from './Assigment.svelte';
  import Context from './Context.svelte';
  import Question from './Question.svelte';

  type ContextItem = {
    type: 'context';
    time: number[];
    title: string;
    items: string[];
  };
  type AssigmentItem = {
    type: 'question';
    time: number[];
    index: number;
    question: string;
    objective: string;
    tracing: {
      title: string;
      items: string[];
    }[];
  };
  type Item = ContextItem | AssigmentItem;

  export let items: Item[];

  const questionsObjetivesTime = items
    .filter(
      (item) =>
        item.type === 'context' ||
        (item.type === 'question' && item.tracing.length == 0)
    )
    .map((item) => Math.max(...item.time))
    .reduce((acc, curr) => acc + curr);

  const questionsTracingTime = items
    .filter((item) => item.type === 'question' && item.tracing.length > 0)
    .map((item) => Math.max(...item.time))
    .reduce((acc, curr) => acc + curr);

  const totalTime = items
    .map((item) => Math.max(...item.time))
    .reduce((acc, curr) => acc + curr);

  let startTime: string = '(a definir comienzo)';
  let endTime: string = `(comienzo + ${totalTime})`;
</script>

<div class="container">
  <div class="grid">
    <p>Tiempo asignado</p>
    <p>Pregunta u objetivo</p>
    <p>Respuesta</p>
  </div>
  {#each items as item, i}
    {#if i === 2 || i === 6 || i === 10}
      <SpacerPDFReady height="8rem" />
    {/if}
    <Assigment time={item.time}>
      {#if item.type === 'context'}
        <Context title={item.title} objectives={item.items} />
      {:else}
        <Question
          index={item.index}
          question={item.question}
          tracing={item.tracing}
          objective={item.objective}
        />
      {/if}
    </Assigment>
  {/each}
  <Assigment time={[questionsObjetivesTime]}>
    <p>Tiempo asignado para preguntas y objetivos</p>
  </Assigment>
  <Assigment time={[questionsTracingTime]}>
    <p>Tiempo asignado para preguntas de seguimiento y redireccion</p>
  </Assigment>
  <Assigment time={[questionsObjetivesTime + questionsTracingTime]}>
    <p>Tiempo asignado para la entrevista {startTime} a {endTime}</p>
  </Assigment>
</div>

<style>
  .container {
    padding: 0rem;
  }
  :global(.grid) {
    display: grid;
    grid-template-columns: 80px 2fr 1fr;
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
