<script lang="ts">
  import SpecificationField from './SpecificationField.svelte';
</script>

<div>
  <ul>
    <li>
      <SpecificationField name="Entrevistado" content="Jeff Bentley" />
    </li>
    <li>
      <SpecificationField name="Fecha" content="19 de enero de 2003" />
    </li>
    <li>
      <SpecificationField name="Hora" content="1:30 p. m." />
    </li>
    <li>
      <SpecificationField
        name="Lugar"
        content="Sala 223, Edificio de administracion"
      />
    </li>
    <li>
      <SpecificationField
        name="Tema"
        content="Politica actual de investigacion de credito"
      />
    </li>
  </ul>
</div>

<style>
  div {
    padding: 1rem;
    border-bottom: 1px solid gray;
  }
</style>
