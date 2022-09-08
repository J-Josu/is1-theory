<script lang="ts">
  import Assigment from './Assigment.svelte';
  import Objective from './Objective.svelte';
  import Question from './Question.svelte';
  export let startTime: string;
  let summary: {
    questiosnObjetivesTime: string;
    questionsTracingTime: string;
    totalTime: string;
  };
  let endTime: string;
</script>

<div class="container">
  <div class="grid">
    <p>Tiempo asignado</p>
    <p>Pregunta u objetivo del administrador</p>
    <p>Respuesta del entrevistado</p>
  </div>
  <Assigment time="1 a 2">
    <Objective
      category="comienza la entrevista"
      objectives={[
        'Nos presentamos',
        'Gracias Sr.Bentley por su valioso tiempo',
        'Enunciar el proposito de la entrevista: obtener una comprension de las politicas existentes de investigacion de credito',
      ]}
    />
  </Assigment>
  <Assigment time="5">
    <Question
      index="0"
      question="¿Que condiciones determinan si se aprueba una solicitud de credito del cliente?"
    />
  </Assigment>
  <Assigment time="5">
    <Question
      index="1"
      question="¿Cuales son las posibles decisiones o acciones que podrian tomarse una vez que estas condiciones han sido evaluadas?"
    />
  </Assigment>
  <Assigment time="3">
    <Question
      index="2"
      question="¿Como se notifica a los clientes cuando no se aprueba su solicitud de credito?"
    />
  </Assigment>
  <Assigment time="1">
    <Question
      index="3"
      question="¿Puedo obtener el permiso para hablar con estas personas para aprender especificamente como llevan a cabo el proceso de investigacion de credito?"
      tracing="Si asi es: ¿Cual seria el momento apropiado para reunirme con cada uno de ellos?"
    />
  </Assigment>
  <Assigment time="1 a 3">
    <Objective
      category="Termino de la entrevista"
      objectives={[
        'Agradezca al Sr. Bentley por su cooperacion y asegurele que estara recibiendo una copia de lo que se obtuvo durante la entrevista.',
      ]}
    />
  </Assigment>
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
    padding: 1rem;
    border-bottom: 1px solid gray;
  }
  :global(.grid) {
    display: grid;
    grid-template-columns: 80px 1fr 1fr;
  }
  :global(.grid > *) {
    border: 1px solid lightgrey;
    padding: 0.25rem;
  }
</style>
