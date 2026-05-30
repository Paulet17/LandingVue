<template>
  <footer class="footer">
    <div class="footer-contenido">

      <div class="footer-marca">
        <div class="footer-logo">
          <i class="fa-solid fa-bag-shopping"></i> Shoply
        </div>
        <p>Tu tienda favorita para comprar con estilo y confianza. Productos premium al mejor precio.</p>
      </div>

      <div class="footer-links">
        <h4>Navegación</h4>
        <ul>
          <li><a href="#inicio">Inicio</a></li>
          <li><a href="#productos">Productos</a></li>
          <li><a href="#beneficios">Beneficios</a></li>
          <li><a href="#registro">Registro</a></li>
        </ul>
      </div>

      <div class="footer-contacto">
        <h4>Contacto</h4>
        <ul>
          <li>contacto@shoply.com</li>
          <li>+1 800 123 4567</li>
          <li>Lun - Vie: 9am - 6pm</li>
        </ul>
      </div>

      <div class="footer-redes">
        <h4>Síguenos</h4>
        <div class="redes-iconos">
          <a href="#"><i class="fa-brands fa-google"></i></a>
          <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
          <a href="#"><i class="fa-brands fa-twitter"></i></a>
        </div>
      </div>

    </div>

    <div class="footer-bottom">
      <p>© 2025 Shoply. Todos los derechos reservados.</p>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: linear-gradient(135deg, #1e1b4b, #312e81);
  color: white;
  padding: 60px 60px 0;
}

.footer-contenido {
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
  justify-content: space-between;
  padding-bottom: 50px;
  border-bottom: 1px solid rgba(255,255,255,0.1);
}

.footer-marca {
  max-width: 280px;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 22px;
  font-weight: bold;
  color: #a855f7;
  margin-bottom: 15px;
}

.footer-marca p {
  font-size: 14px;
  color: rgba(255,255,255,0.6);
  line-height: 1.7;
}

.footer-links h4,
.footer-contacto h4,
.footer-redes h4 {
  font-size: 16px;
  color: white;
  margin-bottom: 20px;
}

.footer-links ul,
.footer-contacto ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.footer-links ul li a {
  text-decoration: none;
  color: rgba(255,255,255,0.6);
  font-size: 14px;
  transition: 0.3s;
}

.footer-links ul li a:hover {
  color: #a855f7;
}

.footer-contacto ul li {
  color: rgba(255,255,255,0.6);
  font-size: 14px;
}

.redes-iconos {
  display: flex;
  gap: 15px;
}

.redes-iconos a {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  background: rgba(255,255,255,0.08);
  display: flex;
  justify-content: center;
  align-items: center;
  color: rgba(255,255,255,0.7);
  font-size: 16px;
  text-decoration: none;
  transition: 0.3s;
}

.redes-iconos a:hover {
  background: #9333ea;
  color: white;
}

.footer-bottom {
  text-align: center;
  padding: 20px 0;
  color: rgba(255,255,255,0.4);
  font-size: 13px;
}

@media(max-width: 768px) {
  .footer {
    padding: 40px 20px 0;
  }
  .footer-contenido {
    gap: 30px;
  }
  .footer-marca {
    max-width: 100%;
  }
}
</style>