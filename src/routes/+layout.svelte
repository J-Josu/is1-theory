<script lang="ts">
  import '../app.css';
  import NavBar from '$cmps/NavBar.svelte';
</script>

<NavBar />

<main>
  <slot />
</main>

<footer>
  <a href="https://github.com/J-Josu/is1-theory">Codigo fuente</a>
</footer>

<style>
  main {
    margin-inline: auto;
    max-width: 95vw;
  }
  @media screen and (min-width: 688px) {
    main {
      max-width: 90vw;
    }
  }
  @media screen and (min-width: 992px) {
    main {
      max-width: 80vw;
    }
  }
  @media screen and (min-width: 1312px) {
    main {
      max-width: 70vw;
    }
  }
  footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 5rem;
    margin-bottom: 1rem;
    width: 100%;
  }
  a {
    width: fit-content;
    font-size: 0.75rem;
    margin: 0.25rem;
    font-style: italic;
    transition: all 0.5s ease-out;
  }
  a:hover {
    font-size: 0.9rem;
    color: var(--dark-green-2);
  }
</style>
