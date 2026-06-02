<script setup>
defineProps({
  value: String
});

const emit = defineEmits(["update:value"]);
</script>

<template>

  <div class="input-group">

    <label>Nombre</label>

    <div class="input-box">

      <i class="fas fa-user icono-input"></i>

      <input
        type="text"
        :value="value"
        placeholder="Ingrese su nombre"
        @input="emit('update:value', $event.target.value)"
      />

    </div>

  </div>

</template>