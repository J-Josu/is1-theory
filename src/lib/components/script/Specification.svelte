<script lang="ts">
  import SpecificationField from './SpecificationField.svelte';
  export let context: {
    name: string;
    date: string;
    hour: string;
    place: string;
    subject: string;
  };
</script>

<div>
  <ul>
    <li>
      <SpecificationField name="Entrevistado" content={context.name} />
    </li>
    <li>
      <SpecificationField name="Fecha" content={context.date} />
    </li>
    <li>
      <SpecificationField name="Hora" content={context.hour} />
    </li>
    <li>
      <SpecificationField name="Lugar" content={context.place} />
    </li>
    <li>
      <SpecificationField name="Tema" content={context.subject} />
    </li>
  </ul>
</div>

<style>
  div {
    padding: 1rem;
  }
</style>
