<script lang="ts">
  import Cover from '$cmps/Cover.svelte';
  import Definitions from '$cmps/technique/Techniques.svelte';
  import Explanation from '$cmps/Explanation.svelte';
  import Questionary from '$cmps/Questionary.svelte';
  import Section from '$cmps/Section.svelte';
  import Script from '$cmps/script/Script.svelte';
  import TeamDescription from '$cmps/teamdescription/TeamDescription.svelte';

  import SpacerPdfReady from '$cmps/pdfready/SpacerPDFReady.svelte';
  import TogglePdfReady from '$cmps/pdfready/TogglePDFReady.svelte';
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

  <SpacerPdfReady height="45vh" />
  <Section
    title={'Cuestionario'}
    subTitle={'Conformacion de los cuestionarios a realizar'}
  >
    <Questionary
      link="https://docs.google.com/forms/d/e/1FAIpQLScKUodXeSGOb1lZDgZqP4QQrLqoAQsR5aKSPtZtpNPj5l-CZA/formResponse"
    />
  </Section>

  <SpacerPdfReady height="25vh" />
  <Section
    title={'Explicacion'}
    subTitle={'Como se realizara el manejo de la informacion a elicitar'}
  >
    <Explanation />
  </Section>

  <SpacerPdfReady height="15vh" />
  <Section
    title={'Otras tecnicas'}
    subTitle={'Formas para obtener mas información, terminologias y referencias'}
  >
    <Definitions />
  </Section>

  <SpacerPdfReady height="62.5vh" />
  <TogglePdfReady />
</article>
