<script setup>
import Swal from "sweetalert2";
import InputNombre from "./inputs/InputNombre.vue";
import InputCorreo from "./inputs/InputCorreo.vue";
import InputPassword from "./inputs/InputPassword.vue";

const registrarUsuario = () => {
  const inputs = document.querySelectorAll("input");
  let vacios = false;
  inputs.forEach((input) => {
    if (input.value.trim() === "") vacios = true;
  });

  if (vacios) {
    Swal.fire({
      icon: "error",
      title: "Campos vacíos",
      text: "Completa todos los campos",
      confirmButtonColor: "#9333ea"
    });
    return;
  }

  Swal.fire({
    icon: "success",
    title: "¡Registro exitoso!",
    text: "Tu cuenta fue creada correctamente",
    confirmButtonColor: "#9333ea"
  });
};
</script>

<template>
  <div class="contenedor">

    <!-- PANEL IZQUIERDO -->
    <div class="panel-izquierdo">

      <div class="logo">
        <i class="fa-solid fa-bag-shopping"></i> Shoply
      </div>

      <span class="badge">
        <i class="fa-solid fa-star"></i> Tu tienda favorita
      </span>

      <h1>Compra con <span>estilo</span> y confianza</h1>

      <p>Únete a nuestra comunidad y disfruta de productos premium con los mejores beneficios.</p>

      <div class="beneficios">

        <div class="beneficio">
          <div class="icono-beneficio">
            <i class="fa-solid fa-truck"></i>
          </div>
          <div>
            <h3>Envíos rápidos</h3>
            <span>A todo el país</span>
          </div>
        </div>

        <div class="beneficio">
          <div class="icono-beneficio">
            <i class="fa-solid fa-shield"></i>
          </div>
          <div>
            <h3>Compra segura</h3>
            <span>Protegemos tus datos</span>
          </div>
        </div>

        <div class="beneficio">
          <div class="icono-beneficio">
            <i class="fa-solid fa-tag"></i>
          </div>
          <div>
            <h3>Ofertas exclusivas</h3>
            <span>Descuentos especiales</span>
          </div>
        </div>

      </div>

      <img
        class="imagen-carrito"
        src="https://cdn-icons-png.flaticon.com/512/3081/3081559.png"
        alt="carrito"
      />

    </div>

    <!-- PANEL DERECHO -->
    <div class="panel-derecho">

      <form class="formulario" @submit.prevent="registrarUsuario">

        <div class="icono-user">
          <i class="fa-solid fa-user"></i>
        </div>

        <h2>¡Crea tu cuenta!</h2>

        <p class="subtitulo">Es rápido, fácil y <span>gratis</span></p>

        <InputNombre />
        <InputCorreo />
        <InputPassword />

        <button type="submit" class="btn-registro">Registrarme</button>

        <div class="linea">
          <span>o continúa con</span>
        </div>

        <div class="social">
          <button type="button" class="social-btn">
            <i class="fa-brands fa-google"></i> Google
          </button>
          <button type="button" class="social-btn">
            <i class="fa-brands fa-facebook-f"></i> Facebook
          </button>
        </div>

        <p class="login">¿Ya tienes cuenta? <span>Inicia sesión</span></p>

      </form>

    </div>

  </div>
</template>