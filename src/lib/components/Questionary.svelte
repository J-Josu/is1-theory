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
  {#if displayAll}
    <p>
      Enlace al cuestionario:
      <a href={link} target="_blank" rel="noopener noreferrer">
        <i>{link}</i>
      </a>
    </p>
    {#each formSections as { src, alt }}
      <img {src} {alt} />
    {/each}
  {:else}
    <a href={link} target="_blank" rel="noopener noreferrer">
      <img src={formSections[0].src} alt={formSections[0].alt} />
    </a>
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
  p {
    max-width: 90%;
  }
  a {
    word-break: break-all;
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
    border: 1px solid lightgray;
    border-radius: 4px;
    text-align: center;
    font-family: inherit;
    opacity: 0.8;
  }
  span {
    font-size: 2rem;
    line-height: 1.25rem;
  }
</style>
