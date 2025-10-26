<template>
  <div class="page-background">
    <v-row class="mt-3 mb-3">
      <v-col cols="12" md="4">
        <v-card
          text="Contribuir a la formación integral de los estudiantes, mediante el desarrollo de procesos afectivos, cognitivos y práxicos."
          title="🎯 Misión"
        ></v-card>
      </v-col>

      <v-col cols="12" md="4">
        <v-card>
          <template v-slot:title>
            Visión
          </template>

          <template v-slot:text>
            La Institución Educativa Comfacor "Jaime Exbrayat", será reconocida por la formación integral de sus estudiantes y su contribución en el desarrollo del contexto local y regional.
          </template>
        </v-card>
      </v-col>

      <v-col cols="12" md="4">
        <v-card>
          <v-card-item>
            <v-card-title> Objetivo General</v-card-title>
          </v-card-item>

          <v-card-text>
            Formar académica, social, moralmente a los estudiantes, mediante la adquisición responsable de conocimientos, habilidades, destrezas, actitudes y valores necesarios para su formación integral y trascendental.
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<style scoped>
.page-background {
  background: linear-gradient(135deg, #e3f2fd 0%, #f5fbff 50%, #ffffff 100%);
  margin: 0;
  padding: 0;
}

/* Estilos originales de las tarjetas (sin cambios) */
:deep(.v-row) {
  margin: 0 !important;
  padding: 12px !important;
}

:deep(.v-card) {
  background: linear-gradient(135deg, #E1F5FE 0%, #FFFFFF 100%) !important;
  border: 2px solid #B3E5FC !important;
  border-radius: 12px !important;
}

:deep(.v-card-title) {
  color: #01579B !important;
  font-weight: 600 !important;
}

:deep(.v-card-text) {
  color: #0277BD !important;
}

:deep(.v-card-item) {
  background-color: #4FC3F7 !important;
}

:deep(.v-card-item .v-card-title) {
  color: #FFFFFF !important;
}
</style>