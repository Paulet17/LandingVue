<script setup>
import { ref } from "vue";

const correo = ref("");
const error = ref("");

const validarCorreo = (valor) => {
  correo.value = valor;
  const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
  if (!regex.test(valor)) {
    error.value = "Ingresa un correo válido";
  } else {
    error.value = "";
  }
};
</script>

<template>
  <div class="input-group">
    <label>Correo electrónico</label>
    <div class="input-box">
      <span class="icono-input">
        <i class="fa-solid fa-envelope"></i>
      </span>
      <input
        type="email"
        placeholder="ejemplo@correo.com"
        :value="correo"
        @input="validarCorreo($event.target.value)"
        :class="error ? 'error-input' : ''"
      />
    </div>
    <p v-if="error" class="error">{{ error }}</p>
  </div>
</template>