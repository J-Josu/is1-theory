<script lang="ts">
  import Explanation from '$cmps/explanation/Explanation.svelte';
  import Questionary from '$cmps/questionary/Questionary.svelte';
  import Script from '$cmps/script/Script.svelte';
  import Section from '$cmps/Section.svelte';
  import TeamData from '$cmps/teamData/TeamData.svelte';
</script>

<div>
  <h1>Trabajo práctico de teoría: 1</h1>

  <h2>Elicitacion de datos para "Cuerpo Fit"</h2>

  <Section title={'Datos'} subTitle={'Informacion del equipo de elicitacion'}>
    <TeamData />
  </Section>

  <Section title={'Guion'} subTitle={'Estructura de la entrevista'}>
    <Script />
  </Section>

  <Section title={'Cuestionario'} subTitle={'Estructura del cuestionario'}>
    <Questionary />
  </Section>

  <Section
    title={'Explicacion'}
    subTitle={'Manejo de la informacion a elicitar'}
  >
    <Explanation />
  </Section>
  <!-- 
  <Section
    title={'Definiciones'}
    subTitle={'Organizacion para la entrevista'}
    description={'7. ¿De qué otra forma puede seguir obteniendo más información? Definan: técnica, forma de realizar y tiempos. Justifique citando bibliografía de los libros de Ingeniería de software sugeridos en la cátedra. Para citar coloque la cita en el texto y al final un apartado de Referencias Bibliográficas bajo la norma APA7 (https://normas-apa.org/)'}
  >
    <ol />
  </Section> -->
</div>

<style>
  div > * {
    text-align: center;
  }
  h1 {
    margin-top: 2rem;
    font-size: 3rem;
  }
  h2 {
    margin-top: 1rem;
    font-size: 2.25rem;
  }
</style>
