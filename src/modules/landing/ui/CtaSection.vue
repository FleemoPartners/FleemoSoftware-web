<template>
  <section class="cta-section">
    <div class="cta-bg-glow"></div>
    <div class="container">
      <h2 class="cta-title">¿Listo para tener tu landing page <span class="text-gradient">profesional</span>?</h2>
      <p class="cta-subtitle">No pierdas más clientes. Empieza a convertir hoy mismo.</p>
      
      <div class="cta-actions">
        <button class="btn-primary">Solicitar cotización ahora</button>
        <button class="btn-secondary">Agenda una llamada de 10 minutos</button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cta-section {
  padding: 120px 20px;
  position: relative;
  overflow: hidden;
  text-align: center;
}

.cta-bg-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at center, rgba(56, 189, 248, 0.15) 0%, transparent 70%);
  pointer-events: none;
  z-index: 0;
}

.container {
  max-width: 800px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.cta-title {
  font-size: 3rem;
  margin-bottom: 24px;
  font-family: var(--font-heading);
}

.cta-subtitle {
  font-size: 1.25rem;
  color: var(--color-text-muted);
  margin-bottom: 40px;
}

.cta-actions {
  display: flex;
  justify-content: center;
  gap: 20px;
  flex-wrap: wrap;
}

.btn-primary {
  background: var(--color-primary);
  color: #000;
  padding: 16px 32px;
  border-radius: 8px;
  font-weight: 700;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  box-shadow: 0 0 20px rgba(56, 189, 248, 0.4);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 0 40px rgba(56, 189, 248, 0.6);
}

.btn-secondary {
  background: rgba(255, 255, 255, 0.05);
  color: var(--color-heading);
  border: 1px solid rgba(255, 255, 255, 0.1);
  padding: 16px 32px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  backdrop-filter: blur(10px);
}

.btn-secondary:hover {
  border-color: var(--color-primary);
  color: var(--color-primary);
  background: rgba(56, 189, 248, 0.1);
}
</style>
