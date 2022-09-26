<script lang="ts">
  import References from './references/References.svelte';
  import Ethnography from './techniques/Ethnography.svelte';
  import Scenaries from './techniques/Scenaries.svelte';
  import UseCases from './techniques/UseCases.svelte';
</script>

<div class="container">
  <div>
    <h3>Tecnicas</h3>
    <p>
      Para obtener mas informacion y/o requerimientos se pueden seguir una o
      varias de las siguientes tecnicas:
    </p>
    <ul>
      <Scenaries />
      <UseCases />
      <Ethnography />
    </ul>
  </div>
  <div>
    <h3>Referencias</h3>
    <References />
  </div>
</div>

<!-- description={'7. ¿De qué otra forma puede seguir obteniendo más información? Definan: técnica, forma de realizar y tiempos. Justifique citando bibliografía de los libros de Ingeniería de software sugeridos en la cátedra. Para citar coloque la cita en el texto y al final un apartado de Referencias Bibliográficas bajo la norma APA7 (https://normas-apa.org/)'} -->
<style>
  .container {
    padding: 0.5rem;
    display: flex;
    flex-direction: column;
    gap: 2rem;
  }
  @media screen and (min-width: 688px) {
    .container {
      margin-inline: auto;
      max-width: 90%;
    }
  }
  .container > div {
    margin-left: 1rem;
    margin-top: 0.5rem;
  }
</style>
