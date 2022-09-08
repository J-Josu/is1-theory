<script lang="ts">
  import Definition from '$cmps/definition/Definition.svelte';
  let link: string = 'https://support.google.com/a/users/answer/9303071?hl=en';
</script>

<div>
  <Definition title="Administracion">
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Veritatis dolore
      perferendis quisquam dolorum facere labore, quos repellat, aperiam amet
      cupiditate voluptatum explicabo. Asperiores, sint similique! Animi qui
      praesentium dolorem similique!
    </p>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Veritatis dolore
      perferendis quisquam dolorum face
    </p>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Veritatis dolore
      perferendis quisquam dolorum facere labore, quos repellat, aperiam amet
      cupiditate voluptatum explicabo. Asperiores, sint similique! Animi qui
      praesentium dolorem similique!
    </p>
  </Definition>
  <Definition title="Obtencion">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi ab,
      similique doloribus dolor labore saepe incidunt placeat omnis impedit
      error vitae deserunt assumenda? Eos ab laudantium dolorem inventore amet
      repudiandae. Lorem ipsum dolor sit amet consectetur adipisicing elit.
      Tempore praesentium nam ut, nostrum eum hic cumque modi libero voluptatum,
      et vitae, velit accusamus tenetur itaque ratione labore reprehenderit
      quasi iure.
    </p>
  </Definition>
</div>

<!-- description={'7. ¿De qué otra forma puede seguir obteniendo más información? Definan: técnica, forma de realizar y tiempos. Justifique citando bibliografía de los libros de Ingeniería de software sugeridos en la cátedra. Para citar coloque la cita en el texto y al final un apartado de Referencias Bibliográficas bajo la norma APA7 (https://normas-apa.org/)'} -->
<style>
  div {
    padding: 0.5rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  p {
    margin-left: 1rem;
    margin-top: 0.5rem;
  }
</style>
