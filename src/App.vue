<template>
  <v-app>
    <v-app-bar color="pink-darken-1">
      <v-toolbar-title>
        <v-btn append-icon="mdi-whatsapp">
        </v-btn>
      </v-toolbar-title>
      <v-btn href="#Nosotros">Nosotros</v-btn>
      <v-btn href="#Servicios">Servicios</v-btn>
      <v-btn href="#Citas">Cita</v-btn>
      <v-btn href="#Contacto" variant="outlined">Contacto</v-btn>
    </v-app-bar>

    <v-main app>
      <v-container>  
        <AboutUs/>
        <Services/>
        <Citas/>
        <Contact/>
      </v-container>

      <v-footer class="d-flex flex-column" app>
        <div class="bg-pink d-flex w-100 align-center px-4">
          <strong>Contactanos en nuestras redes sociales!</strong>

          <v-spacer></v-spacer>

          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            :icon="icon"
            variant="plain"
            size="small"
          ></v-btn>
        </div>

        <div class="px-4 py-2 bg-black text-center w-100">
          {{ new Date().getFullYear() }} — <strong>M404</strong>
        </div>
      </v-footer>
    </v-main>
  </v-app>

</template>

<script setup>
import { ref } from "vue";
import AboutUs from "./components/aboutUs.vue";
import Citas from "./components/citas.vue";
import Contact from "./components/contact.vue";
import Services from "./components/services.vue";

const icons = ref([
  "mdi-whatsapp", 
  "mdi-instagram"

]);
</script>
