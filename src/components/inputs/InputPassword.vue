<script setup>
import { ref } from "vue";

const mostrar = ref(false);
const password = ref("");
const error = ref("");

const validarPassword = (valor) => {
  password.value = valor;
  if (valor.length < 6) {
    error.value = "La contraseña debe tener mínimo 6 caracteres";
  } else {
    error.value = "";
  }
};
</script>

<template>
  <div class="input-group">
    <label>Contraseña</label>
    <div class="input-box">
      <span class="icono-input">
        <i class="fa-solid fa-lock"></i>
      </span>
      <input
        :type="mostrar ? 'text' : 'password'"
        placeholder="Crea una contraseña segura"
        :value="password"
        @input="validarPassword($event.target.value)"
        :class="error ? 'error-input' : ''"
      />
      <button type="button" class="btn-ojo" @click="mostrar = !mostrar">
        <i :class="mostrar ? 'fa-solid fa-eye-slash' : 'fa-solid fa-eye'"></i>
      </button>
    </div>
    <p v-if="error" class="error">{{ error }}</p>
  </div>
</template>