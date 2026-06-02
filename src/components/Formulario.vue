<script setup>
import InputNombre from "./inputs/InputNombre.vue";
import InputCorreo from "./inputs/InputCorreo.vue";
import InputPassword from "./inputs/InputPassword.vue";

defineProps({
  nombre: String,
  correo: String,
  password: String
});

const emit = defineEmits([
  "actualizar-nombre",
  "actualizar-correo",
  "actualizar-password",
  "enviar"
]);
</script>

<template>

  <form
    class="formulario"
    @submit.prevent="emit('enviar')"
  >

    <h2>Crear cuenta</h2>

    <p class="texto-formulario">
      Regístrate para acceder a nuestras promociones.
    </p>

    <InputNombre
      :value="nombre"
      @update:value="emit('actualizar-nombre', $event)"
    />

    <InputCorreo
      :value="correo"
      @update:value="emit('actualizar-correo', $event)"
    />

    <InputPassword
      :value="password"
      @update:value="emit('actualizar-password', $event)"
    />

    <button
      type="submit"
      class="btn"
    >
      Registrarme
    </button>

  </form>

</template>