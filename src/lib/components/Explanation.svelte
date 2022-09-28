<script lang="ts">
</script>

<div class="container">
  <div>
    <h3>Obtencion</h3>
    <p>
      Los cuestionarios como se mostró anteriormente se realizan mediante <a
        href="https://www.google.com/forms/about/"
        target="_blank"
        rel="noopener noreferrer">Google Forms</a
      >
      esto nos permite gestionar todas las respuestas a través de las herramientas
      que ofrece google para ello como lo son la página de gestión del formulario
      activo (en tiempo real) o la posibilidad de generar un
      <a
        href="https://www.google.com/sheets/about/"
        target="_blank"
        rel="noopener noreferrer">Google Sheets</a
      > con toda la información generada para un procesado posterior
    </p>
    <p>
      Estos serán enviados (link de acceso cuestionario web) via mail personal
      de trabajo de cada gerente para que sean respondidos en el plazo de una
      semana
    </p>
    <p>
      Una vez que cada gerente responda su cuestionario automaticamente la
      informacion se sincroniza y está disponible para su procesado por los
      medios anteriormente descriptos, esto nos brinda agilidad a la hora de
      recopilar la informacion y logra que el gerente solo tenga que responderlo
      y no preocuparse por cuestiones aledañas
    </p>
  </div>
  <div>
    <h3>Administracion</h3>
    <p>
      El procesamiento de la información generada sera de manera manual. Esta
      información la podemos clasificar en dos secciones:
    </p>
    <div class="data-type">
      <h4>Datos exactos</h4>
      <p>
        Estos son los valores numéricos como el número de la sucursal, rangos de
        edades entre otros. Con estos podemos generar estadísticas de la cadena
        deportiva en general y de las sucursales puntuales
      </p>
      <p>
        Como la parte que representa este tipo no es mayoritaria dentro de la
        información recaudada no es necesaria la automatización de esta tarea
      </p>
    </div>
    <div class="data-type">
      <h4>Datos no exactos</h4>
      <p>
        Estos son las respuestas abiertas y/o con desarrollo que se realizaron
      </p>
      <p>
        Dado que hay un factor humano/opinion en este tipo es necesario que el
        procesamiento sea manual dado que un humano podra interpretar en el caso
        que la respuesta no sea clara lo que los gerentes que respondieron los
        cuestionarios quisieron transmitir. Ademas que la cantidad de
        cuestionarios a procesar es manejable
      </p>
    </div>
  </div>
</div>

<!-- description={'6. La explicación de cómo se realizará la administración y obtención de resultados de los cuestionarios.'} -->
<style>
  .container {
    display: grid;
    gap: 2rem;
    padding: 0.5rem;
  }
  @media screen and (min-width: 688px) {
    .container {
      margin-inline: auto;
      max-width: 90%;
    }
  }
  @media screen and (min-width: 992px) {
    .container {
      grid-template-columns: 1fr 1fr;
      max-width: none;
    }
  }
  .container > div {
    padding-bottom: 0.5rem;
    border-bottom: 2px solid lightgray;
  }
  p {
    padding-block: 0.5rem;
    padding-inline: 1rem;
  }
  a {
    font-style: italic;
  }
  .data-type {
    margin-left: 1rem;
  }
</style>
