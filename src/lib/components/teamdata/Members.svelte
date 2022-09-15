<script lang="ts">
  import Member from './Member.svelte';
</script>

<div>
  <h3>Integrantes</h3>
  <ul>
    <Member name="Lucas Andres" surname="Gallardo Florido" legajo="19630/4" />
    <Member name="Franco Giovanni" surname="Cirrieli" legajo="19632/6" />
    <Member name="Nicolas" surname="Bonoris" legajo="19413/6" />
    <Member name="Juan Josue" surname="Suarez Arrebola" legajo="20474/6" />
  </ul>
</div>

<style>
  div {
    padding-block: 1rem;
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
</style>
