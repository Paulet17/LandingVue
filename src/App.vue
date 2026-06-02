<script setup>
import { ref } from "vue";
import Swal from "sweetalert2";

import Beneficios from "./components/Beneficios.vue";
import Formulario from "./components/Formulario.vue";
import Footer from "./components/Footer.vue";

const nombre = ref("");
const correo = ref("");
const password = ref("");
const error = ref("");

const manejarSubmit = () => {
  const regexCorreo = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

  if (
    nombre.value.trim() === "" ||
    correo.value.trim() === "" ||
    password.value.trim() === ""
  ) {
    Swal.fire({
      icon: "error",
      title: "Campos vacíos",
      text: "Completa todos los campos",
      confirmButtonColor: "#7e22ce"
    });

    return;
  }

  if (nombre.value.trim().length < 3) {
    Swal.fire({
      icon: "error",
      title: "Nombre inválido",
      text: "El nombre debe tener mínimo 3 letras",
      confirmButtonColor: "#7e22ce"
    });

    return;
  }

  if (!regexCorreo.test(correo.value)) {
    Swal.fire({
      icon: "error",
      title: "Correo inválido",
      text: "Ingresa un correo válido",
      confirmButtonColor: "#7e22ce"
    });

    return;
  }

  if (password.value.length < 6) {
    Swal.fire({
      icon: "error",
      title: "Contraseña inválida",
      text: "La contraseña debe tener mínimo 6 caracteres",
      confirmButtonColor: "#7e22ce"
    });

    return;
  }

  Swal.fire({
    icon: "success",
    title: "Registro exitoso",
    text: "Tu cuenta fue creada correctamente",
    confirmButtonColor: "#7e22ce"
  });

  nombre.value = "";
  correo.value = "";
  password.value = "";
};
</script>

<template>
  <main class="pagina">
    <Beneficios />

    <Formulario
      :nombre="nombre"
      :correo="correo"
      :password="password"
      @actualizar-nombre="nombre = $event"
      @actualizar-correo="correo = $event"
      @actualizar-password="password = $event"
      @enviar="manejarSubmit"
    />
  </main>

  <Footer />
</template>