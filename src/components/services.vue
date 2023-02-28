<template>
  <h1 class="text-center mt-5 mb-5 text-h4 text-uppercase" id="Servicios">Servicios</h1>
  <h1 class="text-center mt-5 mb-5 text-h5">
    Detalles sobre nuestros servicios y precios
  </h1>

  <p class="mb-5">
    En nuestro consultorio médico de ecografías, ofrecemos una amplia variedad
    de servicios de diagnóstico por imágenes que incluyen ecografías 2D,
    doppler, abdominales y de partes blandas.
  </p>

  <div class="d-flex justify-space-around mb-6 bg-surface-variant v-col-auto">
      <v-sheet
        v-for="n in 1"
        :key="n"
        class="ma-2 pa-2"
      >

      <div class="mb-5">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            class="mx-auto"
            color="grey-lighten-4"
            max-width="800"
            v-bind="props"
          >
            <v-img
              :aspect-ratio="16 / 9"
              cover
              src="https://img.freepik.com/foto-gratis/mujer-embarazada-trimestre_53876-139514.jpg"
            >
              <v-expand-transition>
                <div
                  v-if="isHovering"
                  class="d-flex transition-fast-in-fast-out bg-pink-darken-2 v-card--reveal text-h2"
                  style="height: 100%"
                >
                  $14.99
                </div>
              </v-expand-transition>
            </v-img>
    
            <v-card-text class="pt-6">
              <h3 class="text-h4 font-weight-light text-orange mb-2">
                Ecografia 2D
              </h3>
    
              <div class="font-weight-light text-h6 mb-2">
                La ecografía 2D es una técnica de imagen que utiliza ondas sonoras
                para crear imágenes bidimensionales del interior del cuerpo. Esta
                técnica es útil para evaluar la estructura y la función de los
                órganos internos, como el corazón, los riñones, el hígado y los
                ovarios.
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
      </div>
    
      <div class="mb-5">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            class="mx-auto"
            color="grey-lighten-4"
            max-width="800"
            v-bind="props"
          >
            <v-img
              :aspect-ratio="16 / 9"
              cover
              src="https://img.freepik.com/foto-gratis/doctor-revisando-salud-pacientes_23-2148733935.jpg"
            >
              <v-expand-transition>
                <div
                  v-if="isHovering"
                  class="d-flex transition-fast-in-fast-out bg-pink-darken-2 v-card--reveal text-h2"
                  style="height: 100%"
                >
                  $18.99
                </div>
              </v-expand-transition>
            </v-img>
    
            <v-card-text class="pt-6">
              <h3 class="text-h4 font-weight-light text-orange mb-2">Abdominal</h3>
    
              <div class="font-weight-light text-h6 mb-2">
                Las ecografías abdominales son una técnica de imagen que se utiliza
                para evaluar los órganos internos del abdomen, como el hígado, el
                páncreas, los riñones y la vesícula biliar. Esta técnica también
                puede utilizarse para diagnosticar problemas gastrointestinales y de
                la pelvis.
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
      </div>
    
      <div class="mb-5">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            class="mx-auto"
            color="grey-lighten-4"
            max-width="800"
            v-bind="props"
          >
            <v-img
              :aspect-ratio="16 / 9"
              cover
              src="https://diplomadomedico.com/wp-content/uploads/2017/11/adenoma-19.png"
            >
              <v-expand-transition>
                <div
                  v-if="isHovering"
                  class="d-flex transition-fast-in-fast-out bg-pink-darken-2 v-card--reveal text-h2"
                  style="height: 100%"
                >
                  $25.99
                </div>
              </v-expand-transition>
            </v-img>
    
            <v-card-text class="pt-6">
              <h3 class="text-h4 font-weight-light text-orange mb-2">Doppler</h3>
    
              <div class="font-weight-light text-h6 mb-2">
                El doppler es una técnica de imagen que mide la velocidad y
                dirección del flujo sanguíneo. Esta técnica se utiliza comúnmente
                para evaluar la circulación en los vasos sanguíneos, como las
                arterias y venas del cuello, abdomen, piernas y brazos.
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
      </div>
    
      <div class="mb-5">
        <v-hover v-slot="{ isHovering, props }">
          <v-card
            class="mx-auto"
            color="grey-lighten-4"
            max-width="800"
            v-bind="props"
          >
            <v-img
              :aspect-ratio="16 / 9"
              cover
              src="https://centromedicoarasalud.com/wp-content/uploads/2019/09/ECOGRAF%C3%8DA-PARTES-BLANDAS-RODILLA-1.jpg"
            >
              <v-expand-transition>
                <div
                  v-if="isHovering"
                  class="d-flex transition-fast-in-fast-out bg-pink-darken-2 v-card--reveal text-h2"
                  style="height: 100%"
                >
                  $22.99
                </div>
              </v-expand-transition>
            </v-img>
    
            <v-card-text class="pt-6">
              <h3 class="text-h4 font-weight-light text-orange mb-2">
                Partes blandas
              </h3>
    
              <div class="font-weight-light text-h6 mb-2">
                Por último, las ecografías de partes blandas son una técnica de
                imagen que se utiliza para evaluar los músculos, tendones,
                ligamentos y otras estructuras blandas del cuerpo. Esta técnica es
                útil para diagnosticar lesiones musculoesqueléticas y evaluar la
                función de las articulaciones.
              </div>
            </v-card-text>
          </v-card>
        </v-hover>
      </div>



      </v-sheet>
    </div>

</template>

<style>
  .v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .9;
    position: absolute;
    width: 100%;
  }
</style>