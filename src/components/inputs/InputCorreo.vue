<script setup>
defineProps({
  value: String
});

const emit = defineEmits(["update:value"]);
</script>

<template>

  <div class="input-group">

    <label>Correo</label>

    <div class="input-box">

      <i class="fas fa-envelope icono-input"></i>

      <input
        type="email"
        :value="value"
        placeholder="correo@ejemplo.com"
        @input="emit('update:value', $event.target.value)"
      />

    </div>

  </div>

</template>