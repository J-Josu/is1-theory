<script lang="ts">
  import Base from './Base.svelte';
</script>

<Base title="Escenarios">
  <p>
    Los escenarios son particularmente útiles para detallar un bosquejo de
    descripción de requerimientos
  </p>
  <p>
    Se trata de ejemplos sobre descripciones de sesiones de interacción. Cada
    escenario abarca comúnmente una interacción o un número pequeño de
    interacciones posibles
  </p>
  <p>
    Se desarrollan diferentes formas de escenarios y se ofrecen varios tipos de
    información con diversos niveles de detalle acerca del sistema
  </p>
  <p>Un ejemplo de estos escenarios es esta figura sobre historias medicas:</p>
  <figure>
    <img
      src="scenaries.png"
      alt="Figura 4.14 Escenario para recabar historia médica en MHC-PMS"
    />
    <figcaption>
      <i>Nota</i>. Adaptado de Ingeniería de Software, 9° Edición (p. 106), por
      Ian Sommerville , 2011, Pearson.
    </figcaption>
  </figure>
</Base>

<style>
  img {
    width: 100%;
    max-width: 976px;
  }
  figcaption {
    padding-left: 1ch;
  }
</style>
