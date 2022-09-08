<script lang="ts">
  import Members from './Members.svelte';
  import SimpleField from './SimpleField.svelte';
</script>

<div>
  <SimpleField name="numero de grupo" content="grupo 38" />
  <Members />
  <SimpleField name="nombre de grupo" content="solved">
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Alias voluptatem
      commodi quasi ducimus quod incidunt eligendi beatae temporibus error,
      voluptatibus nihil facere vitae cupiditate atque facilis autem ea.
    </p>
  </SimpleField>
</div>

<!-- <h3>Enunciado:</h3>
<p>{contentSummary}</p>  description={'1. Número de grupo.\n2. El nombre , apellido y número de legajo de cada integrante del grupo.\n3. Nombre del equipo de desarrollo, deben buscar un nombre de fantasía para su equipo de desarrollo de software.'}
 -->
<style>
  /* p {
    margin-bottom: 0.5rem;
  } */
</style>
