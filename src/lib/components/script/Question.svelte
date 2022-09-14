<script lang="ts">
  export let index: number=0;
  export let question: string= '';
  export let tracing: string = '';
</script>

<div>
  <h5>Pregunta {index + 1}</h5>
  <p>{question}</p>
  <h5>Seguimiento</h5>
  <p>{tracing}</p>
</div>
