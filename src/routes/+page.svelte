<script lang="ts">
  import Cover from '$cmps/Cover.svelte';
  import Definitions from '$cmps/technique/Techniques.svelte';
  import Explanation from '$cmps/Explanation.svelte';
  import Questionary from '$cmps/Questionary.svelte';
  import Script from '$cmps/script/Script.svelte';
  import Section from '$cmps/Section.svelte';
  import TeamDescription from '$cmps/teamdescription/TeamDescription.svelte';
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
    <TeamDescription />
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
    <Questionary
      link="https://docs.google.com/forms/d/e/1FAIpQLScKUodXeSGOb1lZDgZqP4QQrLqoAQsR5aKSPtZtpNPj5l-CZA/formResponse"
    />
  </Section>

  <Section
    title={'Explicacion'}
    subTitle={'Como se realizara el manejo de la informacion a elicitar'}
  >
    <Explanation />
  </Section>

  <Section
    title={'Otras tecnicas'}
    subTitle={'Formas para obtener mas información, terminologias y referencias'}
  >
    <Definitions />
  </Section>
</article>
