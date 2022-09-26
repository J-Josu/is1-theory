<script lang="ts">
  import BookQuote from './BookQuote.svelte';
  import WebQuote from './WebQuote.svelte';
</script>

<ul>
  <li>
    <WebQuote
      surnameName="Sánchez, C"
      publishDate="06 de agosto de 2019"
      title="¿Cuándo y cuánto citar en APA?"
      siteName="Normas APA (7ma edición)"
      siteURL="https://normas-apa.org/citas/cuando-y-cuanto-citar-en-apa/"
    />
  </li>
  <li>
    <BookQuote
      author="Covey, S. R."
      publishDate="2013"
      title="Los 7 hábitos de las personas altamente efectivas: lecciones poderosas en el cambio personal"
      editorialName="Simon & Schuster"
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
