<script lang="ts">
  import BookQuote from '../references/BookQuote.svelte';
  import Base from './Base.svelte';
</script>

<Base title="Etnografía">
  <p>
    Los sistemas de software no existen aislados; se usan en un contexto social
    y organizacional, dicho escenario podría derivar o restringir los
    requerimientos del sistema, satisfacerlos es crítico para el éxito del mismo
  </p>
  <p>
    Una razón por la que muchos sistemas se entregan, y nunca se utilizan, es
    que sus requerimientos no consideran de manera adecuada cómo afectaría el
    contexto social y organizacional la operación práctica del sistema
  </p>
  <p>
    La etnografía es una técnica de observación que se usa para entender los
    procesos operacionales y ayudar a derivar requerimientos de apoyo para
    dichos procesos
  </p>
  <p>
    Un analista se adentra en el ambiente laboral donde se usará el sistema,
    observa el trabajo diario y toma notas acerca de las tareas existentes en
    que intervienen los participantes. La técnica ayuda a descubrir
    requerimientos implícitos que reflejan las formas actuales en que trabaja la
    gente, ya que las personas encuentran muy difícil articular los detalles de
    su trabajo, los factores sociales y organizacionales que afectan el trabajo
    se vuelven claros cuando los percibe un observador sin prejuicios
  </p>
  <div class="subsection">
    <h4>Ventajas</h4>
    <p>
      La etnografía es muy efectiva para descubrir dos tipos de requerimientos:
    </p>
    <ul>
      <li><p>La forma en que realmente trabaja la gente</p></li>
      <li>
        <p>
          La cooperación y el conocimiento de las actividades de otras personas
        </p>
      </li>
    </ul>
  </div>
  <div class="subsection">
    <h4>Desventajas</h4>
    <p>
      No siempre es adecuado para descubrir requerimientos de la organización o
      de dominio
    </p>
    <p>
      No en todos los casos se identifican nuevas características que deben
      agregarse a un sistema
    </p>
    <p>
      No es un enfoque completo y debe usarse para complementar otros enfoques,
      como el análisis de casos de uso
    </p>
  </div>
  <div class="subsection">
    <h4>Conclusión</h4>
    <p>
      Las prácticas reales del trabajo son más ricas, más complejas y más
      dinámicas que los modelos simples supuestos por los sistemas de
      automatización administrativa
    </p>
    <p>
      La diferencia entre el trabajo supuesto y el real fue la razón más
      importante por la que dichos sistemas de oficina no tenían un efecto
      significativo sobre la productividad
    </p>
  </div>

  <BookQuote
    author="Ian Sommerville"
    publishDate="2011"
    title="Ingeniería de Software, 9° Edición"
    editorialName="Pearson"
  />
</Base>

<style>
  .subsection p {
    margin-left: 1rem;
    margin-top: 0.5rem;
  }
  h4 {
    font-weight: 500;
  }
  ul {
    margin-left: 1rem;
  }
  li {
    margin-top: 0.25rem;
    margin-left: 0.5rem;
  }
  li::marker {
    content: '-';
  }
</style>
