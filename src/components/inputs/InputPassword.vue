<script setup>
import { ref } from "vue";

defineProps({
  value: String
});

const emit = defineEmits(["update:value"]);

const mostrar = ref(false);
</script>

<template>

  <div class="input-group">

    <label>Contraseña</label>

    <div class="password-box">

      <i class="fas fa-lock icono-input"></i>

      <input
        :type="mostrar ? 'text' : 'password'"
        :value="value"
        placeholder="Ingrese contraseña"
        @input="emit('update:value', $event.target.value)"
      />

      <button
        type="button"
        class="btn-ojo"
        @click="mostrar = !mostrar"
      >

        <i
          :class="
            mostrar
              ? 'fas fa-eye-slash'
              : 'fas fa-eye'
          "
        ></i>

      </button>

    </div>

  </div>

</template>