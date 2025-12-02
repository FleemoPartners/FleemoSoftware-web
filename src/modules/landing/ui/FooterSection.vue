<template>
  <footer class="footer-section">
    <div class="container">
      <div class="footer-top">
        <div class="footer-brand">
          <div class="footer-logo">
            <!-- Logo placeholder -->
            <span class="logo-text">Fleemo<span class="text-gradient">Software</span></span>
          </div>
          <p class="brand-desc">
            Desarrollo de software y landing pages de alto impacto para empresas que quieren crecer.
          </p>
        </div>
        
        <div class="footer-links">
          <div class="link-group">
            <h4>Menú</h4>
            <ul>
              <li><a href="#">Inicio</a></li>
              <li><a href="#">Servicios</a></li>
              <li><a href="#">Portfolio</a></li>
              <li><a href="#">Contacto</a></li>
            </ul>
          </div>
          
          <div class="link-group">
            <h4>Contacto</h4>
            <ul>
              <li><a href="mailto:contacto@fleemosoftware.com">contacto@fleemosoftware.com</a></li>
              <li><a href="#">WhatsApp: +123 456 7890</a></li>
              <li class="hours">Lun - Vie: 9:00 - 18:00</li>
            </ul>
          </div>
          
          <div class="link-group">
            <h4>Legal</h4>
            <ul>
              <li><a href="#">Términos y Condiciones</a></li>
              <li><a href="#">Política de Privacidad</a></li>
            </ul>
          </div>
        </div>
      </div>
      
      <div class="footer-bottom">
        <p>&copy; {{ new Date().getFullYear() }} FleemoSoftware. Todos los derechos reservados.</p>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer-section {
  background: #020617; /* Deepest black/blue */
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  padding: 80px 20px 40px;
  position: relative;
}

.footer-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, var(--color-primary), transparent);
  opacity: 0.3;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.footer-top {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 60px;
  margin-bottom: 60px;
}

.footer-logo {
  font-size: 1.5rem;
  font-weight: 800;
  margin-bottom: 20px;
  display: inline-block;
  font-family: var(--font-heading);
}

.brand-desc {
  color: var(--color-text-muted);
  max-width: 300px;
}

.footer-links {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

.link-group h4 {
  font-size: 1.1rem;
  margin-bottom: 20px;
  color: var(--color-heading);
  font-family: var(--font-heading);
}

.link-group ul {
  list-style: none;
  padding: 0;
}

.link-group li {
  margin-bottom: 12px;
}

.link-group a {
  color: var(--color-text-muted);
  transition: color 0.3s ease;
}

.link-group a:hover {
  color: var(--color-primary);
}

.hours {
  color: var(--color-text-muted);
  opacity: 0.7;
}

.footer-bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  padding-top: 40px;
  text-align: center;
  color: var(--color-text-muted);
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .footer-top {
    grid-template-columns: 1fr;
  }
  
  .footer-links {
    grid-template-columns: 1fr;
    gap: 40px;
  }
}
</style>
