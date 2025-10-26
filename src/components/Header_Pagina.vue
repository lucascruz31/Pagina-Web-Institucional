<template>
  <v-app-bar :elevation="2" height="150" class="custom-header">
    <template v-slot:prepend>
      <!-- Eliminado el v-app-bar-nav-icon -->
    </template>
    
    <v-img 
      class="mx-auto my-6" 
      max-width="100px" 
      src="https://comfacor.com.co/newweb/wp-content/uploads/2022/07/MANUAL-CORPORATIVO-COMFACOR.png"
    ></v-img>

    <v-app-bar-title></v-app-bar-title>
    
    <template v-slot:append>
      <v-btn class="login-button" @click="dialog = true">Iniciar Sesion</v-btn>
    </template>
  </v-app-bar>

  <v-dialog v-model="dialog" width="600px">
    <LoginApp></LoginApp>
  </v-dialog>  
</template>

<script setup>
  import { ref } from 'vue'
  const dialog = ref(false)
</script>

<style scoped>
.custom-header {
  background: linear-gradient(135deg, #e3f2fd 0%, #f5fbff 50%, #ffffff 100%) !important;
  border-bottom: 3px solid #b3e5fc !important;
  box-shadow: 0 4px 12px rgba(179, 229, 252, 0.3) !important;
}

.login-button {
  background: linear-gradient(135deg, #4fc3f7 0%, #29b6f6 100%) !important;
  color: white !important;
  border-radius: 25px !important;
  padding: 12px 24px !important;
  font-weight: 600 !important;
  text-transform: none !important;
  box-shadow: 0 4px 8px rgba(41, 182, 246, 0.3) !important;
  transition: all 0.3s ease !important;
}

.login-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 12px rgba(41, 182, 246, 0.4) !important;
  background: linear-gradient(135deg, #29b6f6 0%, #039be5 100%) !important;
}

:deep(.v-img) {
  filter: drop-shadow(0 2px 4px rgba(0, 0, 0, 0.1));
  transition: transform 0.3s ease;
}

:deep(.v-img:hover) {
  transform: scale(1.05);
}
</style>