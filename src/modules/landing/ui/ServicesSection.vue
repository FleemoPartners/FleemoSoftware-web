<template>
  <section class="services-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Nuestros <span class="text-gradient">Planes</span></h2>
        <p class="section-subtitle">Soluciones escalables para cada etapa de tu negocio.</p>
      </div>
      
      <div class="plans-grid">
        <!-- Basic Plan -->
        <div class="plan-card">
          <div class="plan-header">
            <h3 class="plan-name">Básico</h3>
            <p class="plan-desc">Ideal para validar ideas o productos.</p>
            <div class="plan-price-placeholder">Consultar Precio</div>
          </div>
          
          <ul class="plan-features">
            <li>✅ Landing Page Sencilla</li>
            <li>✅ Diseño Responsive</li>
            <li>✅ Botones de WhatsApp</li>
            <li>✅ Entrega en 72h</li>
          </ul>
          
          <button class="btn-plan">Elegir este plan</button>
        </div>
        
        <!-- Professional Plan -->
        <div class="plan-card popular">
          <div class="popular-tag">Más Popular</div>
          <div class="plan-header">
            <h3 class="plan-name">Profesional</h3>
            <p class="plan-desc">Para negocios que buscan crecer.</p>
            <div class="plan-price-placeholder">Consultar Precio</div>
          </div>
          
          <ul class="plan-features">
            <li>✅ Todo lo del Básico</li>
            <li>✅ Secciones Extra</li>
            <li>✅ Animaciones Smooth</li>
            <li>✅ Integraciones (Mailchimp, etc)</li>
            <li>✅ Entrega en 48h</li>
          </ul>
          
          <button class="btn-plan primary">Elegir este plan</button>
        </div>
        
        <!-- Enterprise Plan -->
        <div class="plan-card">
          <div class="plan-header">
            <h3 class="plan-name">Empresa</h3>
            <p class="plan-desc">Solución completa y personalizada.</p>
            <div class="plan-price-placeholder">Consultar Precio</div>
          </div>
          
          <ul class="plan-features">
            <li>✅ Todo lo del Profesional</li>
            <li>✅ Diseño Premium Exclusivo</li>
            <li>✅ Formularios Avanzados</li>
            <li>✅ Base de Datos + Hosting</li>
            <li>✅ Soporte Prioritario</li>
          </ul>
          
          <button class="btn-plan">Elegir este plan</button>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services-section {
  padding: var(--section-gap) 20px;
  position: relative;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-header {
  text-align: center;
  margin-bottom: 60px;
}

.section-title {
  font-size: 2.5rem;
  margin-bottom: 16px;
}

.section-subtitle {
  color: var(--color-text-muted);
}

.plans-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  align-items: start;
}

.plan-card {
  background: rgba(30, 41, 59, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  border-radius: 16px;
  padding: 40px;
  position: relative;
  transition: all 0.3s ease;
}

.plan-card:hover {
  border-color: rgba(56, 189, 248, 0.3);
  transform: translateY(-5px);
}

.plan-card.popular {
  background: rgba(30, 41, 59, 0.6);
  border-color: var(--color-primary);
  box-shadow: 0 0 40px -10px rgba(56, 189, 248, 0.2);
  transform: scale(1.05);
  z-index: 1;
}

.plan-card.popular:hover {
  transform: scale(1.05) translateY(-5px);
  box-shadow: 0 0 50px -10px rgba(56, 189, 248, 0.3);
}

.popular-tag {
  position: absolute;
  top: -12px;
  left: 50%;
  transform: translateX(-50%);
  background: var(--color-primary);
  color: #000;
  padding: 4px 12px;
  border-radius: 20px;
  font-size: 0.8rem;
  font-weight: 700;
  box-shadow: 0 0 15px rgba(56, 189, 248, 0.5);
}

.plan-header {
  text-align: center;
  margin-bottom: 30px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  padding-bottom: 30px;
}

.plan-name {
  font-size: 1.5rem;
  margin-bottom: 8px;
  font-family: var(--font-heading);
}

.plan-desc {
  color: var(--color-text-muted);
  font-size: 0.9rem;
  margin-bottom: 20px;
}

.plan-price-placeholder {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--color-primary);
}

.plan-features {
  list-style: none;
  padding: 0;
  margin: 0 0 30px 0;
}

.plan-features li {
  margin-bottom: 12px;
  color: var(--color-text);
  display: flex;
  align-items: center;
  gap: 10px;
}

.btn-plan {
  width: 100%;
  padding: 12px;
  border-radius: 8px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  color: var(--color-heading);
  font-weight: 600;
  transition: all 0.3s ease;
  background: rgba(255, 255, 255, 0.05);
}

.btn-plan:hover {
  border-color: var(--color-primary);
  color: var(--color-primary);
  background: rgba(56, 189, 248, 0.1);
}

.btn-plan.primary {
  background: var(--color-primary);
  color: #000;
  border: none;
  box-shadow: 0 0 20px rgba(56, 189, 248, 0.3);
}

.btn-plan.primary:hover {
  background: #0ea5e9; /* Darker sky blue */
  box-shadow: 0 0 30px rgba(56, 189, 248, 0.5);
}
</style>
