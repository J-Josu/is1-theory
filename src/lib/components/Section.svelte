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
    text-align: center;
    max-width: 80%;
  }
  main {
    align-self: center;
    width: 100%;
    padding-top: 2rem;
  }
  @media screen and (min-width: 688px) {
    main {
      width: 95%;
    }
  }
  @media screen and (min-width: 992px) {
    main {
      width: 90%;
    }
  }
</style>
