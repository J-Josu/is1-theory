<script lang="ts">
  export let members: {
    name: string;
    surname: string;
    legajo: string;
  }[];
</script>

<div>
  <h3>Integrantes</h3>
  <ul>
    {#each members as { name, surname, legajo }}
      <li>
        <p><b>Nombre:</b> {name}</p>
        <p><b>Apellido:</b> {surname}</p>
        <p><b>Legajo:</b> {legajo}</p>
      </li>
    {/each}
  </ul>
</div>

<style>
  div {
    padding-block: 1rem;
    margin-left: 5%;
    margin-right: 5%;
  }
  @media screen and (min-width: 688px) {
    div {
      margin: 0;
    }
  }
  h3 {
    margin-top: 1rem;
    font-size: 1.5rem;
  }
  ul {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
    column-gap: 2rem;
    row-gap: 1rem;
    margin-top: 1rem;
    margin-left: 1rem;
  }
  @media screen and (min-width: 688px) {
    ul {
      grid-template-columns: repeat(2, 1fr);
    }
  }
  li {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    border: 1px solid gray;
    border-radius: 1rem;
    padding: 2rem;
  }
  p {
    font-size: 1rem;
  }
</style>
