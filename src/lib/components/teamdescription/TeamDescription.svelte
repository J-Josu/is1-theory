<script lang="ts">
  import Members from './Members.svelte';
  import SimpleField from './SimpleField.svelte';

  import data from '$lib/data/team.json';
</script>

<div>
  <SimpleField name="numero de grupo" content={data.group_number.toString()} />
  <Members members={data.members} />
  <SimpleField name="nombre de grupo" content={data.name}>
    <p>
      Nosotros queriamos encontrar un sentido que describa nuestro proposito
      ademas de querer que el nombre contenga algo relacionado al ambito de la
      informatica. Para ello despues de un brain storming encontrados la palabra
      justa que define nuestro fin a alcanzar solved (resuelto, conteniendo sol
      representando a la bandera argentina) incluyendo la palabra dev (developer
      - desarollador) escrito a la inversa
    </p>
  </SimpleField>
</div>

<!-- description={'1. Número de grupo.\n2. El nombre , apellido y número de legajo de cada integrante del grupo.\n3. Nombre del equipo de desarrollo, deben buscar un nombre de fantasía para su equipo de desarrollo de software.'} -->
<style>
  p {
    font-size: 1.06rem;
  }
</style>
