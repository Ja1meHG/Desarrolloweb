<template>
    <form @submit.prevent="submit">
      <div class="form-group">
        <label for="nombre">Nombre:</label>
        <input
          type="text"
          id="nombre"
          v-model="nombre"
          pattern="[A-Za-záéíóúÁÉÍÓÚüÜñÑ\s]+"
          required
          class="rounded-input"
        />
        <span v-if="nombreInvalido" class="error-message">
          El nombre no puede contener números.
        </span>
        <span v-if="nombreIguales" class="error-message">
          El nombre y el apellido no pueden ser iguales.
        </span>
      </div>
      <!-- Agrega aquí más campos y elementos del formulario si es necesario -->
      <button type="submit">Enviar</button>
    </form>
  </template>
  
  <script>
  export default {
    data() {
      return {
        nombre: "",
        nombreInvalido: false,
        nombreIguales: false,
      };
    },
    methods: {
      submit() {
        // Lógica de manejo del formulario
        // Puedes realizar validaciones y enviar datos al servidor aquí
      },
    },
  };
  </script>
  