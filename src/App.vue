<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Productos from './components/Productos.vue'
import Beneficios from './components/Beneficios.vue'
import Formulario from './components/Formulario.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <Navbar />
  <section id="inicio">
    <Hero />
  </section>
  <section id="productos">
    <Productos />
  </section>
  <section id="beneficios">
    <Beneficios />
  </section>
  <section id="registro">
    <div class="container">
      <Formulario />
    </div>
  </section>
  <Footer />
</template>