<script setup>
import { ref } from "vue";

const nombre = ref("");
const error = ref("");

const validarNombre = (valor) => {
  nombre.value = valor;
  if (valor.trim().length < 3) {
    error.value = "El nombre debe tener mínimo 3 letras";
  } else {
    error.value = "";
  }
};
</script>

<template>
  <div class="input-group">
    <label>Nombre completo</label>
    <div class="input-box">
      <span class="icono-input">
        <i class="fa-solid fa-user"></i>
      </span>
      <input
        type="text"
        placeholder="Ingresa tu nombre y apellido"
        :value="nombre"
        @input="validarNombre($event.target.value)"
        :class="error ? 'error-input' : ''"
      />
    </div>
    <p v-if="error" class="error">{{ error }}</p>
  </div>
</template>