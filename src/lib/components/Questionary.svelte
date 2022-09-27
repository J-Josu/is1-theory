<script lang="ts">
  export let link: string;

  let displayAll = true;

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
      <div class="window"><img {src} {alt} /></div>
    {/each}
  {:else}
    <a href={link} target="_blank" rel="noopener noreferrer">
      <div class="window">
        <img src={formSections[0].src} alt={formSections[0].alt} />
      </div>
    </a>
  {/if}
  <button
    class:printing={displayAll}
    on:click={() => (displayAll = !displayAll)}
    ><span>{displayAll ? '-' : '+'}</span>
  </button>
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
  .window {
    justify-items: center;
    overflow: hidden;
    max-width: 976px;
  }
  img {
    width: 175%;
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
    opacity: 0.5;
  }
  button.printing {
    opacity: 0;
  }
  button:hover {
    opacity: 1;
  }
  span {
    font-size: 2rem;
    line-height: 1.25rem;
  }
</style>
