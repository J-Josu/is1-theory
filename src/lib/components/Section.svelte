<script lang="ts">
  export let title: string;
  export let subTitle: string;
</script>

<section>
  <header>
    <h1>{title}</h1>
    <p>{subTitle}</p>
  </header>
  <main>
    <slot />
  </main>
</section>

<style>
  section {
    display: flex;
    flex-direction: column;
    margin-top: 3rem;
    padding-block: 1rem;
    padding-inline: 0.25rem;
  }
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-block: 1rem;
  }
  header > h1 {
    font-size: 2rem;
  }
  header > p {
    margin-top: 0.25rem;
    font-size: 1.25rem;
  }
  main {
    align-self: center;
    width: 92.5%;
    padding-top: 2rem;
  }
</style>
