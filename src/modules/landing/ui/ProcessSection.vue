<template>
  <section class="process-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Cómo <span class="text-gradient">Trabajamos</span></h2>
        <p class="section-subtitle">Un proceso simple y transparente para resultados excepcionales.</p>
      </div>
      
      <div class="process-steps">
        <div class="step-card" v-for="(step, index) in steps" :key="index">
          <div class="step-number">{{ index + 1 }}</div>
          <div class="step-content">
            <h3 class="step-title">{{ step.title }}</h3>
            <p class="step-desc">{{ step.desc }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  {
    title: 'Brief del Cliente',
    desc: 'Cuéntanos tu idea. Elegimos estilo, colores y secciones juntos.'
  },
  {
    title: 'Propuesta Visual',
    desc: 'En 12h–24h te presentamos una propuesta de diseño para tu aprobación.'
  },
  {
    title: 'Desarrollo + Optimización',
    desc: 'Construimos tu sitio con código limpio y lo optimizamos para SEO.'
  },
  {
    title: 'Entrega + Soporte',
    desc: 'Lanzamos tu web y te damos soporte para asegurar que todo funcione.'
  }
]
</script>

<style scoped>
.process-section {
  padding: var(--section-gap) 20px;
  position: relative;
}

.container {
  max-width: 1000px;
  margin: 0 auto;
}

.section-header {
  text-align: center;
  margin-bottom: 80px;
}

.section-title {
  font-size: 2.5rem;
  margin-bottom: 16px;
}

.section-subtitle {
  color: var(--color-text-muted);
}

.process-steps {
  display: flex;
  flex-direction: column;
  gap: 40px;
  position: relative;
}

.process-steps::before {
  content: '';
  position: absolute;
  left: 24px;
  top: 0;
  bottom: 0;
  width: 2px;
  background: linear-gradient(to bottom, transparent, var(--color-primary), transparent);
  z-index: 0;
  box-shadow: 0 0 15px var(--color-primary);
}

.step-card {
  display: flex;
  gap: 30px;
  align-items: flex-start;
  position: relative;
  z-index: 1;
}

.step-number {
  width: 50px;
  height: 50px;
  background: var(--color-background);
  border: 2px solid var(--color-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--color-primary);
  flex-shrink: 0;
  box-shadow: 0 0 20px rgba(56, 189, 248, 0.5);
  text-shadow: 0 0 10px rgba(56, 189, 248, 0.5);
}

.step-content {
  background: rgba(30, 41, 59, 0.4);
  backdrop-filter: blur(10px);
  padding: 24px;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  flex-grow: 1;
  transition: all 0.3s ease;
}

.step-content:hover {
  border-color: rgba(56, 189, 248, 0.3);
  transform: translateX(10px);
  box-shadow: 0 10px 30px -10px rgba(0, 0, 0, 0.5);
  background: rgba(30, 41, 59, 0.6);
}

.step-title {
  font-size: 1.25rem;
  margin-bottom: 8px;
  color: var(--color-heading);
  font-family: var(--font-heading);
}

.step-desc {
  color: var(--color-text-muted);
}

@media (min-width: 768px) {
  .process-steps::before {
    left: 50%;
    transform: translateX(-50%);
  }
  
  .step-card {
    width: 50%;
    margin-left: auto;
    padding-left: 40px;
  }
  
  .step-card:nth-child(odd) {
    margin-left: 0;
    margin-right: auto;
    flex-direction: row-reverse;
    padding-left: 0;
    padding-right: 40px;
    text-align: right;
  }
  
  .step-number {
    position: absolute;
    left: -25px; /* Half width */
  }
  
  .step-card:nth-child(odd) .step-number {
    left: auto;
    right: -25px;
  }
  
  .step-content:hover {
    transform: translateY(-5px);
  }
}
</style>
