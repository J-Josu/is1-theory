<script lang="ts">
  import Frame from '$cmps/explanation/Frame.svelte';
  let link: string = 'https://support.google.com/a/users/answer/9303071?hl=en';
</script>

<div>
  <Frame title="Administracion">
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
  </Frame>
  <Frame title="Obtencion">
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi ab,
      similique doloribus dolor labore saepe incidunt placeat omnis impedit
      error vitae deserunt assumenda? Eos ab laudantium dolorem inventore amet
      repudiandae. Lorem ipsum dolor sit amet consectetur adipisicing elit.
      Tempore praesentium nam ut, nostrum eum hic cumque modi libero voluptatum,
      et vitae, velit accusamus tenetur itaque ratione labore reprehenderit
      quasi iure.
    </p>
  </Frame>
</div>

<!-- description={'6. La explicación de cómo se realizará la administración y obtención de resultados de los cuestionarios.'} -->
<style>
  div {
    padding: 0.5rem;
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  p {
    margin-left: 1rem;
    margin-top: 0.5rem;
  }
</style>
