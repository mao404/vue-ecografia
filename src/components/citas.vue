<template>
  <v-cointainer>
    <h1 class="text-center mt-5 mb-5 text-h4 text-uppercase" id="Citas">Citas</h1>
    <h1 class="text-center mt-5 mb-5 text-h5">
      Agenda una cita con nosotros!
    </h1>
    <form @submit.prevent="submit">
    <v-text-field
      v-model="name.value.value"
      :counter="10"
      :error-messages="name.errorMessage.value"
      label="Nombre"
    ></v-text-field>

    <v-text-field
      v-model="phone.value.value"
      :counter="7"
      :error-messages="phone.errorMessage.value"
      label="Teléfono"
    ></v-text-field>

    <v-text-field
      v-model="email.value.value"
      :error-messages="email.errorMessage.value"
      label="Correo Electrónico"
    ></v-text-field>

    <v-select
      v-model="select.value.value"
      :items="items"
      :error-messages="select.errorMessage.value"
      label="Servicio"
    ></v-select>

    <v-btn
      class="me-4"
      type="submit"
    >
      enviar
    </v-btn>

    <v-btn @click="handleReset">
      limpiar
    </v-btn>
  </form>
  </v-cointainer>
</template>

<script>
  import { ref } from 'vue'
  import { useField, useForm } from 'vee-validate'

  export default {
    setup () {
      const { handleSubmit, handleReset } = useForm({
        validationSchema: {
          name (value) {
            if (value?.length >= 2) return true

            return 'El nombre debe ser de al menos 2 caracteres.'
          },
          phone (value) {
            if (value?.length > 9 && /[0-9-]+/.test(value)) return true

            return 'El número telefonico debe ser de al menos 9 digitos.'
          },
          email (value) {
            if (/^[a-z0-9.-]+@[a-z.-]+\.[a-z]+$/i.test(value)) return true

            return 'Debe ser un correo válido.'
          },
          select (value) {
            if (value) return true

            return 'Seleccione un servicio.'
          },
        },
      })
      const name = useField('name')
      const phone = useField('phone')
      const email = useField('email')
      const select = useField('select')
      const checkbox = useField('checkbox')

      const items = ref([
        'Ecografia 2D',
        'Abdominal',
        'Doppler',
        'Partes blandas',
      ])

      const submit = handleSubmit(values => {
        alert(JSON.stringify(values, null, 2))
      })

      return { name, phone, email, select, items, submit, handleReset }
    },
  }
</script>