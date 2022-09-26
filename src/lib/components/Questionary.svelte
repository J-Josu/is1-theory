<script lang="ts">
  export let link: string;

  let displayAll = false;

  const formSections = new Array(7).fill({}).map((_, i) => {
    return {
      src: `googleform/page-${i + 1}.png`,
      alt: `Pagina ${i + 1} del cuestionario`,
    };
  });
</script>

<div>
  <a href={link} target="_blank" rel="noopener noreferrer">
    <img src={formSections[0].src} alt={formSections[0].alt} />
  </a>
  {#if displayAll}
    {#each formSections.slice(1) as { src, alt }}
      <img {src} {alt} />
    {/each}
  {/if}
  <button on:click={() => (displayAll = !displayAll)}
    ><span>{displayAll ? '-' : '+'}</span></button
  >
</div>

<!-- description={'5. Un cuestionario para los/las gerentes de cada local. Definirlo adecuadamente según lo visto en teoría con, a lo sumo 20 preguntas'} -->
<style>
  div {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
  }
  img {
    width: 100%;
    max-width: 976px;
  }
  button {
    align-self: flex-end;
    padding-block: 0.5rem;
    padding-inline: 1rem;
    background: none;
    opacity: 0.8;
    border: 1px solid lightgray;
    border-radius: 4px;
    text-align: center;
    font-family: inherit;
  }
  span {
    font-size: 2rem;
    line-height: 1.25rem;
  }
</style>
