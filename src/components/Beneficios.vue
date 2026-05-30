<template>
  <div class="beneficios-seccion">
    <h2 class="seccion-titulo">¿Por qué elegir <span>Shoply</span>?</h2>
    <p class="seccion-subtitulo">Todo lo que necesitas en un solo lugar</p>
    <div class="beneficios-grid">
      <div class="beneficio-card">
        <div class="beneficio-icono"><i class="fa-solid fa-truck"></i></div>
        <h3>Envíos rápidos</h3>
        <p>Recibe tus productos en menos de 48 horas a cualquier parte del país.</p>
      </div>
      <div class="beneficio-card">
        <div class="beneficio-icono"><i class="fa-solid fa-shield"></i></div>
        <h3>Compra segura</h3>
        <p>Tus datos y pagos están protegidos con encriptación de última generación.</p>
      </div>
      <div class="beneficio-card">
        <div class="beneficio-icono"><i class="fa-solid fa-tag"></i></div>
        <h3>Ofertas exclusivas</h3>
        <p>Accede a descuentos y promociones especiales solo para miembros.</p>
      </div>
      <div class="beneficio-card">
        <div class="beneficio-icono"><i class="fa-solid fa-headset"></i></div>
        <h3>Soporte 24/7</h3>
        <p>Nuestro equipo está disponible en todo momento para ayudarte.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.beneficios-seccion {
  padding: 100px 60px;
  text-align: center;
  background: rgba(255,255,255,0.4);
  backdrop-filter: blur(10px);
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
  margin-bottom: 50px;
}

.beneficios-grid {
  display: flex;
  justify-content: center;
  gap: 25px;
  flex-wrap: wrap;
}

.beneficio-card {
  background: white;
  border-radius: 25px;
  padding: 40px 30px;
  width: 240px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  box-shadow: 0 8px 25px rgba(139,92,246,0.1);
  transition: 0.3s;
}

.beneficio-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 35px rgba(139,92,246,0.18);
}

.beneficio-icono {
  width: 75px;
  height: 75px;
  border-radius: 50%;
  background: linear-gradient(135deg, #f5ecff, #ead7ff);
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 28px;
  color: #9333ea;
  margin-bottom: 20px;
  box-shadow: 0 5px 15px rgba(168,85,247,0.15);
}

.beneficio-card h3 {
  font-size: 18px;
  color: #1e1b4b;
  margin-bottom: 12px;
}

.beneficio-card p {
  font-size: 14px;
  color: #6b7280;
  line-height: 1.6;
}

@media(max-width: 768px) {
  .beneficios-seccion {
    padding: 70px 20px;
  }
  .seccion-titulo {
    font-size: 34px;
  }
}
</style>