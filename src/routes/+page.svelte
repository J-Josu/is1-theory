<script lang="ts">
  import Definitions from '$cmps/definition/Definitions.svelte';
  import Explanation from '$cmps/explanation/Explanation.svelte';
  import Questionary from '$cmps/questionary/Questionary.svelte';
  import Script from '$cmps/script/Script.svelte';
  import Section from '$cmps/Section.svelte';
  import TeamData from '$cmps/teamData/TeamData.svelte';
</script>

<svelte:head>
  <title>Solved</title>
  <link rel="icon" href="/argentinian_flag_sun.svg" />
</svelte:head>

<div>
  <h1>Trabajo práctico de teoría: 1</h1>

  <h2>Elicitacion de datos para "Cuerpo Fit"</h2>

  <Section
    title={'Datos'}
    subTitle={'Informacion sobre el equipo de desarrollo'}
  >
    <TeamData />
  </Section>

  <Section
    title={'Guion'}
    subTitle={'Estructura a seguir durante la entrevista'}
  >
    <Script />
  </Section>

  <Section
    title={'Cuestionario'}
    subTitle={'Conformacion de los cuestionarios a realizar'}
  >
    <Questionary />
  </Section>

  <Section
    title={'Explicacion'}
    subTitle={'Como se realizara el manejo de la informacion a elicitar'}
  >
    <Explanation />
  </Section>

  <Section
    title={'Definiciones'}
    subTitle={'Desarrollo de terminologia y referencias'}
  >
    <Definitions />
  </Section>
</div>

<style>
  h1 {
    margin-top: 2rem;
    font-size: 3rem;
    text-align: center;
  }
  h2 {
    margin-top: 1rem;
    font-size: 2.25rem;
    text-align: center;
  }
</style>
