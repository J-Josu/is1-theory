<script lang="ts">
  export let name: string;
  export let surname: string;
  export let legajo: string;
</script>

<li class="field-group">
  <p><b>Nombre:</b> {name}</p>
  <p><b>Apellido:</b> {surname}</p>
  <p><b>Legajo:</b> {legajo}</p>
</li>

<style>
  .field-group {
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
