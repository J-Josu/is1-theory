<script lang="ts">
</script>

<div class="container">
  <div>
    <h3>Obtencion:</h3>
    <p>
      Los cuestionarios como se mostraron anteriormente son mediante <a
        href="https://www.google.com/forms/about/"
        target="_blank"
        rel="noopener noreferrer">Google Forms</a
      >
      esto nos permite gestionar todas las respuestas a travez de las herramientas
      que ofrece google para ello como lo son la pagina de gestion del formulario
      activo (en tiempo real) o la posibilidad de generar un
      <a
        href="https://www.google.com/sheets/about/"
        target="_blank"
        rel="noopener noreferrer">Google Sheets</a
      > con toda la informacion generada para un procesado posterior
    </p>
  </div>
  <div>
    <h3>Administracion:</h3>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Veritatis dolore
      perferendis quisquam dolorum facere labore, quos repellat, aperiam amet
      cupiditate voluptatum explicabo. Asperiores, sint similique! Animi qui
      praesentium dolorem similique!
    </p>
  </div>
</div>

<!-- description={'6. La explicación de cómo se realizará la administración y obtención de resultados de los cuestionarios.'} -->
<style>
  .container {
    padding: 0.5rem;
    display: grid;
    gap: 2rem;
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
    border-bottom: 2px solid lightgray;
  }
  p {
    position: relative;
    margin-top: 0.5rem;
    padding: 0 1rem 1rem 1rem;
  }
  a {
    font-style: italic;
  }
</style>
