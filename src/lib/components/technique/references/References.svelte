<script lang="ts">
  import BookQuote from './BookQuote.svelte';
</script>

<ul>
  <li>
    <BookQuote
      author="Ian Sommerville"
      publishDate="2011"
      title="Ingeniería de Software, 9° Edición"
      editorialName="Pearson"
    />
  </li>
</ul>

<style>
  ul {
    margin-left: 0.5rem;
    margin-top: 0.25rem;
  }
  li {
    margin-left: 0.5rem;
    padding-left: 0.5rem;
  }
  li::marker {
    content: '-';
    margin-left: 0.25rem;
  }
</style>
