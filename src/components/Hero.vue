<template>
  <div class="hero">
    <div class="hero-texto">
      <div class="logo">
        <i class="fa-solid fa-bag-shopping"></i> Shoply
      </div>
      <span class="badge">
        <i class="fa-solid fa-star"></i> Tu tienda favorita
      </span>
      <h1>Compra con <span>estilo</span> y confianza</h1>
      <p>Únete a nuestra comunidad y disfruta de productos premium con los mejores beneficios.</p>
      <a href="#registro" class="hero-btn">Crear cuenta gratis</a>
    </div>
    <div class="hero-imagen">
      <img
        src="https://cdn-icons-png.flaticon.com/512/3081/3081559.png"
        alt="carrito"
      />
    </div>
  </div>
</template>

<style scoped>
.hero {
  min-height: 100vh;
  padding: 120px 60px 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
  background: linear-gradient(180deg, #f5ecff, #ead7ff, #dcb8ff);
}

.hero-texto {
  max-width: 600px;
  display: flex;
  flex-direction: column;
}

.logo {
  width: fit-content;
  padding: 14px 20px;
  border-radius: 15px;
  background: white;
  font-size: 28px;
  font-weight: bold;
  color: #7e22ce;
  box-shadow: 0 5px 15px rgba(0,0,0,0.08);
}

.badge {
  display: inline-block;
  margin-top: 30px;
  background: rgba(168,85,247,0.15);
  color: #9333ea;
  padding: 10px 18px;
  border-radius: 50px;
  font-weight: 600;
  width: fit-content;
}

h1 {
  margin-top: 25px;
  font-size: 65px;
  line-height: 1.1;
  color: #1e1b4b;
}

h1 span {
  color: #9333ea;
}

p {
  margin-top: 20px;
  font-size: 20px;
  line-height: 1.7;
  color: #5b21b6;
}

.hero-btn {
  margin-top: 35px;
  width: fit-content;
  padding: 16px 35px;
  background: linear-gradient(135deg, #7c3aed, #a855f7);
  color: white;
  border-radius: 50px;
  text-decoration: none;
  font-weight: bold;
  font-size: 17px;
  transition: 0.3s;
  box-shadow: 0 8px 25px rgba(168,85,247,0.35);
}

.hero-btn:hover {
  transform: translateY(-3px);
}

.hero-imagen img {
  width: 380px;
  max-width: 100%;
}

@media(max-width: 900px) {
  .hero {
    flex-direction: column;
    text-align: center;
    padding: 100px 30px 50px;
    align-items: center;
  }
  h1 {
    font-size: 45px;
  }
  .hero-btn {
    align-self: center;
  }
  .hero-imagen img {
    width: 250px;
  }
}

@media(max-width: 480px) {
  h1 {
    font-size: 32px;
  }
  .hero-imagen {
    display: none;
  }
}
</style>