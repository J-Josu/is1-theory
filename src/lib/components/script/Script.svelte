<script lang="ts">
  import Assigments from './Assigments.svelte';
  import Comments from './Comments.svelte';
  import Specification from './Specification.svelte';

  let comments: string[] = [
    'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, voluptatibus iure consequatur sint velit veritatis aperiam natus corporis eos eaque.',
    'Lorem adipisicing elit. Magnam, quis?',
    'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam magni qui assumenda ',
  ];
</script>

<div>
  <Specification />
  <Assigments startTime="1 a 2 min." />
  <Comments {comments} />
</div>

<!-- description={'4. El guión de una entrevista para la gerente general, según el esquema visto en teoría'} -->
<style>
  div {
    border: 1px solid gray;
    border-radius: 1px;
    padding: 0.5rem;
    margin-top: 2rem;
  }
</style>
