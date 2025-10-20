<template>
  <v-app-bar :elevation="2"
  height=150>
  <template v-slot:prepend>
    <v-app-bar-nav-icon></v-app-bar-nav-icon>
  </template>
   <v-img class="mx-auto my-6" max-width="100px" src="https://comfacor.com.co/newweb/wp-content/uploads/2022/07/MANUAL-CORPORATIVO-COMFACOR.png"></v-img>

  <v-app-bar-title></v-app-bar-title>
  <template v-slot:append>
          <v-btn  @click="dialog = true">Iniciar Sesion</v-btn>
        </template>
</v-app-bar>

 <v-dialog
      v-model="dialog"
      width="600px"
    >
       <LoginApp></LoginApp>
  </v-dialog>  
</template>
<script setup>
  import { ref } from 'vue'
     const dialog = ref(false)
</script>