<script setup>
const productos = [
  {
    id: 1,
    nombre: "Zapatillas Urban",
    precio: "$89.99",
    imagen: "https://cdn-icons-png.flaticon.com/512/2589/2589175.png",
    categoria: "Calzado"
  },
  {
    id: 2,
    nombre: "Mochila Premium",
    precio: "$59.99",
    imagen: "https://cdn-icons-png.flaticon.com/512/3321/3321752.png",
    categoria: "Accesorios"
  },
  {
    id: 3,
    nombre: "Reloj Clásico",
    precio: "$129.99",
    imagen: "https://cdn-icons-png.flaticon.com/512/2972/2972531.png",
    categoria: "Joyería"
  }
];
</script>

<template>
  <div class="productos-seccion">
    <h2 class="seccion-titulo">Productos <span>destacados</span></h2>
    <p class="seccion-subtitulo">Los favoritos de nuestra comunidad</p>
    <div class="productos-grid">
      <div
        class="producto-card"
        v-for="p in productos"
        :key="p.id"
      >
        <div class="producto-img">
          <img :src="p.imagen" :alt="p.nombre" />
        </div>
        <span class="producto-categoria">{{ p.categoria }}</span>
        <h3>{{ p.nombre }}</h3>
        <p class="producto-precio">{{ p.precio }}</p>
        <button class="producto-btn">Ver producto</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.productos-seccion {
  padding: 100px 60px;
  text-align: center;
}

.seccion-titulo {
  font-size: 48px;
  color: #1e1b4b;
  margin-bottom: 10px;
}

.seccion-titulo span {
  color: #9333ea;
}

.seccion-subtitulo {
  font-size: 18px;
  color: #6b7280;
  margin-bottom: 60px;
}

.productos-grid {
  display: flex;
  justify-content: center;
  gap: 30px;
  flex-wrap: wrap;
}

.producto-card {
  background: rgba(255,255,255,0.85);
  border-radius: 25px;
  padding: 35px 30px;
  width: 280px;
  display: flex;
  flex-direction: column;
  align-items: center;
  box-shadow: 0 10px 30px rgba(139,92,246,0.12);
  transition: 0.3s;
  backdrop-filter: blur(10px);
}

.producto-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 40px rgba(139,92,246,0.2);
}

.producto-img {
  width: 130px;
  height: 130px;
  background: linear-gradient(135deg, #f5ecff, #ead7ff);
  border-radius: 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 20px;
}

.producto-img img {
  width: 80px;
}

.producto-categoria {
  font-size: 12px;
  color: #9333ea;
  font-weight: 600;
  background: rgba(168,85,247,0.1);
  padding: 5px 14px;
  border-radius: 50px;
  margin-bottom: 12px;
}

.producto-card h3 {
  font-size: 20px;
  color: #1e1b4b;
  margin-bottom: 8px;
}

.producto-precio {
  font-size: 22px;
  font-weight: bold;
  color: #7c3aed;
  margin-bottom: 20px;
}

.producto-btn {
  width: 100%;
  padding: 12px;
  border: 2px solid #9333ea;
  border-radius: 50px;
  background: transparent;
  color: #9333ea;
  font-weight: 600;
  font-size: 15px;
  cursor: pointer;
  transition: 0.3s;
}

.producto-btn:hover {
  background: linear-gradient(135deg, #7c3aed, #a855f7);
  color: white;
  border-color: transparent;
}

@media(max-width: 768px) {
  .productos-seccion {
    padding: 70px 20px;
  }
  .seccion-titulo {
    font-size: 34px;
  }
}
</style>