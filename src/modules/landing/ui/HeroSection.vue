<template>
  <section class="hero-section">
    <div class="hero-bg-glow"></div>

    <div class="container">
      <div class="hero-content">
        <h1 class="hero-title">
          Landing Pages Profesionales en
          <span class="text-gradient">Tiempo Récord</span>
        </h1>
        <p class="hero-subtitle">
          Diseños personalizados, optimizados y creados por ingenieros expertos.
        </p>

        <div class="hero-actions">
          <button class="btn-primary">Solicitar Cotización</button>
          <button class="btn-secondary">Ver Plantillas</button>
        </div>

        <div class="trust-badges">
          <div class="badge">
            <span class="badge-icon">👥</span>
            <span>+40 clientes satisfechos</span>
          </div>
          <div class="badge">
            <span class="badge-icon">🚀</span>
            <span>Entregas en 24–72 horas</span>
          </div>
        </div>
      </div>

      <div class="hero-image">
        <div class="mockup-container">
          <!-- Placeholder for mockup -->
          <div class="mockup-screen">
            <div class="mockup-header">
              <div class="dot red"></div>
              <div class="dot yellow"></div>
              <div class="dot green"></div>
            </div>
            <div class="mockup-body">
              <div class="skeleton-hero"></div>
              <div class="skeleton-content">
                <div class="line"></div>
                <div class="line"></div>
                <div class="line short"></div>
              </div>
            </div>
          </div>
          <div class="glow-effect"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  position: relative;
  padding: 120px 20px 80px;
  display: flex;
  justify-content: center;
  overflow: hidden;
}

.hero-bg-glow {
  position: absolute;
  top: -20%;
  left: 50%;
  transform: translateX(-50%);
  width: 80%;
  height: 600px;
  background: radial-gradient(
    circle,
    var(--color-primary-glow) 0%,
    transparent 70%
  );
  opacity: 0.4;
  z-index: 0;
  pointer-events: none;
}

.container {
  max-width: 1200px;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  z-index: 1;
}

.hero-content {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.hero-title {
  font-size: 3.5rem;
  line-height: 1.1;
  letter-spacing: -0.02em;
}

.hero-subtitle {
  font-size: 1.25rem;
  color: var(--color-text-muted);
  max-width: 500px;
}

.hero-actions {
  display: flex;
  gap: 16px;
  margin-top: 16px;
}

.btn-primary {
  background: var(--color-primary);
  color: #000;
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.3s ease;
  box-shadow: 0 0 20px rgba(56, 189, 248, 0.3);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 0 30px rgba(56, 189, 248, 0.5);
}

.btn-secondary {
  background: transparent;
  color: var(--color-heading);
  border: 1px solid var(--color-border);
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 600;
  font-size: 1rem;
  transition: all 0.3s ease;
}

.btn-secondary:hover {
  border-color: var(--color-primary);
  color: var(--color-primary);
}

.trust-badges {
  display: flex;
  gap: 24px;
  margin-top: 32px;
  font-size: 0.9rem;
  color: var(--color-text-muted);
}

.badge {
  display: flex;
  align-items: center;
  gap: 8px;
}

.hero-image {
  position: relative;
}

.mockup-container {
  position: relative;
  transform: perspective(1000px) rotateY(-5deg) rotateX(5deg);
  transition: transform 0.5s ease;
}

.mockup-container:hover {
  transform: perspective(1000px) rotateY(0deg) rotateX(0deg);
}

.mockup-screen {
  background: var(--color-background-soft);
  border: 1px solid var(--color-border);
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5);
}

.mockup-header {
  background: var(--color-background-mute);
  padding: 12px;
  display: flex;
  gap: 8px;
  border-bottom: 1px solid var(--color-border);
}

.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
}

.dot.red {
  background: #ef4444;
}
.dot.yellow {
  background: #eab308;
}
.dot.green {
  background: #22c55e;
}

.mockup-body {
  padding: 20px;
  height: 300px;
  display: flex;
  flex-direction: column;
  gap: 16px;
  background: linear-gradient(
    180deg,
    var(--color-background-soft) 0%,
    #000 100%
  );
}

.skeleton-hero {
  height: 120px;
  background: var(--color-background-mute);
  border-radius: 8px;
  width: 100%;
}

.skeleton-content .line {
  height: 12px;
  background: var(--color-background-mute);
  border-radius: 4px;
  margin-bottom: 8px;
}

.skeleton-content .line.short {
  width: 60%;
}

.glow-effect {
  position: absolute;
  inset: -20px;
  background: var(--color-primary);
  filter: blur(60px);
  opacity: 0.2;
  z-index: -1;
}

@media (max-width: 768px) {
  .container {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .hero-content {
    align-items: center;
  }

  .hero-title {
    font-size: 2.5rem;
  }

  .hero-actions {
    justify-content: center;
  }

  .trust-badges {
    justify-content: center;
    flex-wrap: wrap;
  }

  .hero-image {
    margin-top: 40px;
  }
}
</style>
