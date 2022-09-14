<script lang="ts">
  import Assigments from './Assigments.svelte';
  import Comments from './Comments.svelte';
  import Specification from './Specification.svelte';

  import data from './data.json';
</script>

<div>
  <Specification context={data.context} />
  <Assigments startTime={[1, 2]} items={data.script} />
  <Comments comments={data.notes} />
</div>

<!-- description={'4. El guión de una entrevista para la gerente general, según el esquema visto en teoría'} -->
<style>
  div {
    border: 1px solid gray;
    border-radius: 1px;
    margin-top: 2rem;
  }

  @media screen and (min-width: 688px) {
    div {
      padding: 0.5rem;
    }
  }
</style>
