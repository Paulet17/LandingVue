<template>
  <nav class="navbar">
    <div class="navbar-logo">
      <i class="fa-solid fa-bag-shopping"></i> Shoply
    </div>
    <ul class="navbar-links">
      <li><a href="#inicio">Inicio</a></li>
      <li><a href="#productos">Productos</a></li>
      <li><a href="#beneficios">Beneficios</a></li>
      <li><a href="#registro" class="nav-btn">Registro</a></li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 100;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 18px 60px;
  background: rgba(255, 255, 255, 0.85);
  backdrop-filter: blur(15px);
  box-shadow: 0 2px 20px rgba(139, 92, 246, 0.1);
}

.navbar-logo {
  font-size: 22px;
  font-weight: bold;
  color: #7e22ce;
  display: flex;
  align-items: center;
  gap: 10px;
}

.navbar-links {
  list-style: none;
  display: flex;
  gap: 35px;
  margin: 0;
  padding: 0;
}

.navbar-links a {
  text-decoration: none;
  color: #312e81;
  font-weight: 600;
  font-size: 15px;
  transition: 0.3s;
}

.navbar-links a:hover {
  color: #9333ea;
}

.navbar-links .nav-btn {
  background: linear-gradient(135deg, #7c3aed, #a855f7);
  color: white;
  padding: 10px 22px;
  border-radius: 50px;
}

.navbar-links .nav-btn:hover {
  color: white;
  transform: translateY(-2px);
  box-shadow: 0 5px 15px rgba(168, 85, 247, 0.4);
}

@media(max-width: 768px) {
  .navbar {
    padding: 15px 20px;
  }
  .navbar-links {
    gap: 15px;
  }
  .navbar-links a {
    font-size: 13px;
  }
}

@media(max-width: 480px) {
  .navbar-links li:not(:last-child) {
    display: none;
  }
}
</style>