<template>
<<<<<<< HEAD
  <div class="page-background">
    <v-row class="d-flex justify-center mt-10">
      <div class="text-center">
        <h1 class="display-1 font-weight-bold mb-4 title-gradient">Nuestra Historia</h1>
      </div>
    </v-row>
    <v-row class="d-flex justify-center">
      <v-col cols="12" md="8" lg="6">
        <v-timeline align="start" class="custom-timeline">
          <v-timeline-item
            v-for="(year, i) in years"
            :key="i"
            :dot-color="year.color"
            size="small"
          >
            <template v-slot:opposite>
              <div
                :class="`pt-1 headline font-weight-bold year-text`"
                v-text="year.year"
              ></div>
            </template>
            <div class="timeline-card">
              <h2 :class="`mt-n1 headline font-weight-light mb-4 timeline-title`">
                {{ year.titulo }}
              </h2>
              <div class="timeline-content">
                {{ year.texto }}
              </div>
            </div>
          </v-timeline-item>
        </v-timeline>
      </v-col>
    </v-row>
  </div>
=======
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
>>>>>>> 422988babc9f2724943b0e4a388ee58b3245b7fc
</template>

<script setup>
  const years = [
    {
      color: '#4FC3F7',
      year: '(1984 - 1990)',
      titulo: 'Fundación y primeros años',
      texto: 'El Colegio Comfacor fue fundado por la Caja de Compensación Familiar de Córdoba (Comfacor) con el propósito de brindar educación de calidad a los hijos de los afiliados.',
    },
    {
<<<<<<< HEAD
      color: '#29B6F6',
=======
      color: '#87CEEB',
>>>>>>> 422988babc9f2724943b0e4a388ee58b3245b7fc
      year: '(1991 - 2000)',
      titulo: 'Crecimiento académico',
      texto: 'Se amplió la cobertura educativa hasta la educación básica secundaria, se implementaron proyectos pedagógicos orientados al desarrollo social y comunitario y el colegio comenzó a ganar reconocimiento local por su calidad educativa.'
    },
    {
<<<<<<< HEAD
      color: '#03A9F4',
=======
      color: '#B3E5FC',
>>>>>>> 422988babc9f2724943b0e4a388ee58b3245b7fc
      year: '(2001 - 2010)',
      titulo: 'Consolidación institucional',
      texto: 'Se incorporaron nuevas infraestructuras y recursos tecnológicos, se fortalecieron las áreas de ciencias, inglés y competencias ciudadanas y el colegio reafirmó su compromiso con la formación integral bajo los valores de solidaridad, respeto y responsabilidad.',
    },
    {
<<<<<<< HEAD
      color: '#0288D1',
=======
      color: '#4FC3F7',
>>>>>>> 422988babc9f2724943b0e4a388ee58b3245b7fc
      year: '(2011 - 2020)',
      titulo: 'Innovación educativa',
      texto: 'Se adoptaron metodologías activas e inclusivas que promueven el aprendizaje significativo, se impulsaron programas de educación ambiental, arte y cultura e inició la integración de TIC en el proceso de enseñanza-aprendizaje.',
    },
    {
<<<<<<< HEAD
      color: '#01579B',
=======
      color: '#87CEEB',
>>>>>>> 422988babc9f2724943b0e4a388ee58b3245b7fc
      year: '(2021 - Actualidad)',
      titulo: 'Proyección y calidad',
      texto: 'El colegio continúa posicionándose como una institución educativa líder en Córdoba, se fortalecen los programas de formación en valores, bilingüismo y tecnología y su misión sigue centrada en formar ciudadanos competentes, solidarios y comprometidos con el desarrollo social.',
    },
  ]
</script>

<style scoped>
<<<<<<< HEAD
.page-background {
  background: linear-gradient(135deg, #e3f2fd 0%, #f5fbff 50%, #ffffff 100%);
  min-height: 100vh;
  padding: 20px 0;
  margin: 0;
}

.title-gradient {
  background: linear-gradient(135deg, #01579B 0%, #03A9F4 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.custom-timeline {
  padding: 20px 0;
}

.timeline-card {
  background: linear-gradient(135deg, #FFFFFF 0%, #F5FBFF 100%) !important;
  border: 2px solid #B3E5FC !important;
  border-radius: 16px !important;
  padding: 24px !important;
  box-shadow: 0 4px 12px rgba(179, 229, 252, 0.3) !important;
  transition: all 0.3s ease !important;
  position: relative;
  overflow: hidden;
}

.timeline-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  background: linear-gradient(180deg, #4FC3F7 0%, #01579B 100%);
}

.timeline-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 8px 20px rgba(179, 229, 252, 0.5) !important;
}

.timeline-title {
  color: #01579B !important;
  font-weight: 500 !important;
}

.timeline-content {
  color: #0277BD !important;
  line-height: 1.6;
  font-size: 1rem;
}

.year-text {
  color: #0288D1 !important;
  background: rgba(179, 229, 252, 0.2);
  padding: 8px 16px;
  border-radius: 20px;
  border: 1px solid #B3E5FC;
}

:deep(.v-timeline-item__dot) {
  box-shadow: 0 0 0 4px #FFFFFF, 0 0 0 8px currentColor !important;
  transition: all 0.3s ease !important;
}

:deep(.v-timeline-item__dot:hover) {
  transform: scale(1.2);
  box-shadow: 0 0 0 4px #FFFFFF, 0 0 0 10px currentColor !important;
=======
:deep(.v-timeline-item__body) {
  background: #FFFFFF !important;
  border: 2px solid #B3E5FC !important;
  border-radius: 12px !important;
  padding: 20px !important;
>>>>>>> 422988babc9f2724943b0e4a388ee58b3245b7fc
}

:deep(.v-timeline-divider__before),
:deep(.v-timeline-divider__after) {
  background-color: #B3E5FC !important;
}

<<<<<<< HEAD
:deep(.v-timeline-item__body) {
  background: transparent !important;
}

/* Responsive */
@media (max-width: 960px) {
  :deep(.v-timeline-item:not(:last-child) .v-timeline-item__body) {
    margin-bottom: 24px;
  }
  
  .timeline-card {
    padding: 20px !important;
  }
}

@media (max-width: 600px) {
  .page-background {
    padding: 15px 0;
  }
  
  .timeline-card {
    padding: 16px !important;
  }
  
  .year-text {
    font-size: 0.9rem !important;
    padding: 6px 12px;
  }
=======
:deep(.v-timeline-item__dot) {
  box-shadow: 0 0 0 4px #FFFFFF, 0 0 0 8px currentColor !important;
}

:deep(.text-\\#4FC3F7) {
  color: #4FC3F7 !important;
}

:deep(.text-\\#87CEEB) {
  color: #87CEEB !important;
}

:deep(.text-\\#B3E5FC) {
  color: #0277BD !important;
}

.display-1 {
  color: #01579B !important;
>>>>>>> 422988babc9f2724943b0e4a388ee58b3245b7fc
}
</style>