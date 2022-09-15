<script lang="ts">
  import Cover from '$cmps/Cover.svelte';
  import Definitions from '$cmps/definition/Definitions.svelte';
  import Explanation from '$cmps/explanation/Explanation.svelte';
  import Questionary from '$cmps/questionary/Questionary.svelte';
  import Script from '$cmps/script/Script.svelte';
  import Section from '$cmps/Section.svelte';
  import TeamData from '$cmps/teamdata/TeamData.svelte';
</script>

<svelte:head>
  <title>Solved</title>
  <link rel="icon" href="/argentinian_flag_sun.svg" />
</svelte:head>

<article>
  <Cover />

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
</article>
