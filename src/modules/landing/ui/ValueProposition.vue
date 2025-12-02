<template>
  <section class="value-prop-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">
          ¿Por qué <span class="text-gradient">FleemoSoftware</span>?
        </h2>
        <p class="section-subtitle">
          Nos diferenciamos por la calidad técnica y la velocidad de entrega.
        </p>
      </div>

      <div class="features-grid">
        <div
          class="feature-card"
          v-for="(feature, index) in features"
          :key="index"
        >
          <div class="feature-icon">{{ feature.icon }}</div>
          <h3 class="feature-title">{{ feature.title }}</h3>
          <p class="feature-desc">{{ feature.desc }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    icon: "⚡",
    title: "Entregas Ultrarrápidas",
    desc: "Tu landing page lista en 24–72 horas sin sacrificar calidad.",
  },
  {
    icon: "🎨",
    title: "Diseño Personalizado",
    desc: "Nada de plantillas genéricas. Diseño visual adaptado a tu marca.",
  },
  {
    icon: "🧪",
    title: "100% Funcional",
    desc: "Probado rigurosamente y optimizado para maximizar conversiones.",
  },
  {
    icon: "📱",
    title: "Totalmente Responsive",
    desc: "Se ve perfecto en móviles, tablets y escritorio.",
  },
  {
    icon: "🧑‍💻",
    title: "Ingenieros Expertos",
    desc: "Desarrollado por profesionales con experiencia real en software.",
  },
  {
    icon: "🔍",
    title: "SEO + Carga Rápida",
    desc: "Optimizamos el código para que Google te ame y tus usuarios no esperen.",
  },
];
</script>

<style scoped>
.value-prop-section {
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
  font-size: 1.1rem;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
}

.feature-card {
  background: rgba(30, 41, 59, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.05);
  padding: 30px;
  border-radius: 16px;
  transition: all 0.4s ease;
  position: relative;
  overflow: hidden;
  backdrop-filter: blur(10px);
}

.feature-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at top right, rgba(56, 189, 248, 0.1), transparent 40%);
  opacity: 0;
  transition: opacity 0.4s ease;
}

.feature-card:hover {
  border-color: rgba(56, 189, 248, 0.3);
  transform: translateY(-5px);
  box-shadow: 0 10px 40px -10px rgba(0, 0, 0, 0.5);
}

.feature-card:hover::before {
  opacity: 1;
}

.feature-icon {
  font-size: 2.5rem;
  margin-bottom: 20px;
  background: rgba(56, 189, 248, 0.1);
  width: 60px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  border: 1px solid rgba(56, 189, 248, 0.2);
}

.feature-title {
  font-size: 1.25rem;
  margin-bottom: 12px;
  color: var(--color-heading);
}

.feature-desc {
  color: var(--color-text-muted);
  line-height: 1.6;
}
</style>
