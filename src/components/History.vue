<template>
<v-row class="d-flex justify-center margin-top-10">
  <div class="text-center">
    <h1 class="display-1 font-weight-bold mb-4">Nuestra Historia</h1>
  </div>
</v-row>
<v-row class="d-flex justify-center">
  <v-col cols="6">
  <v-timeline align="start">
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :dot-color="year.color"
      size="small"
    >
      <template v-slot:opposite>
        <div
          :class="`pt-1 headline font-weight-bold text-${year.color}`"
          v-text="year.year"
        ></div>
      </template>
      <div>
        <h2 :class="`mt-n1 headline font-weight-light mb-4 text-${year.color}`">
          {{ year.titulo }}
        </h2>
        <div>
          {{ year.texto }}
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
</v-col>

</v-row>
  
</template>
<script setup>
  const years = [
    {
      color: 'yellow',
      year: '(1984 - 1990)',
      titulo: 'Fundación y primeros años',
      texto: 'El Colegio Comfacor fue fundado por la Caja de Compensación Familiar de Córdoba (Comfacor) con el propósito de brindar educación de calidad a los hijos de los afiliados.',
    },
    {
      color: 'blue lighten-3',
      year: '(1991 - 2000)',
      titulo: 'Crecimiento académico',
      texto: 'Se amplió la cobertura educativa hasta la educación básica secundaria, se implementaron proyectos pedagógicos orientados al desarrollo social y comunitario y el colegio comenzó a ganar reconocimiento local por su calidad educativa.'
    },
    {
      color: 'white',
      year: '(2001 - 2010)',
      titulo: 'Consolidación institucional',
      texto: 'Se incorporaron nuevas infraestructuras y recursos tecnológicos, se fortalecieron las áreas de ciencias, inglés y competencias ciudadanas y el colegio reafirmó su compromiso con la formación integral bajo los valores de solidaridad, respeto y responsabilidad.',
    },
    {
      color: 'yellow',
      year: '(2011 - 2020)',
      titulo: 'Innovación educativa',
      texto: 'Se adoptaron metodologías activas e inclusivas que promueven el aprendizaje significativo, se impulsaron programas de educación ambiental, arte y cultura e inició la integración de TIC en el proceso de enseñanza-aprendizaje.',
    },
    {
      color: 'blue lighten-3',
      year: '(2021 - Actualidad)',
      titulo: 'Proyección y calidad',
      texto: 'El colegio continúa posicionándose como una institución educativa líder en Córdoba, se fortalecen los programas de formación en valores, bilingüismo y tecnología y su misión sigue centrada en formar ciudadanos competentes, solidarios y comprometidos con el desarrollo social.',
    },
  ]
</script>