<template>
  <section class="tech-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Tecnologías Modernas</h2>
        <p class="section-subtitle">
          Usamos tecnologías modernas para garantizar velocidad, seguridad y escalabilidad.
        </p>
      </div>
      
      <div class="tech-grid">
        <div class="tech-item" v-for="tech in techs" :key="tech.name" :title="tech.name">
          <img :src="tech.icon" :alt="tech.name" class="tech-icon" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import vueLogo from '@/assets/vue.svg'
import astroLogo from '@/assets/astro.svg'
import reactLogo from '@/assets/react.svg'
import nextjsLogo from '@/assets/nextjs.svg'
import html5Logo from '@/assets/html5.svg'
import css3Logo from '@/assets/css3.svg'
import tailwindLogo from '@/assets/tailwind.svg'

const techs = [
  {
    name: 'Vue.js',
    icon: vueLogo
  },
  {
    name: 'Astro',
    icon: astroLogo
  },
  {
    name: 'React',
    icon: reactLogo
  },
  {
    name: 'Next.js',
    icon: nextjsLogo
  },
  {
    name: 'HTML5',
    icon: html5Logo
  },
  {
    name: 'CSS3',
    icon: css3Logo
  },
  {
    name: 'Tailwind CSS',
    icon: tailwindLogo
  }
]
</script>

<style scoped>
.tech-section {
  padding: 80px 20px;
  background: linear-gradient(180deg, #000 0%, #0f172a 100%);
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  position: relative;
}

.tech-section::before {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at center, rgba(56, 189, 248, 0.05) 0%, transparent 70%);
  pointer-events: none;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  text-align: center;
}

.section-title {
  font-size: 2rem;
  margin-bottom: 16px;
}

.section-subtitle {
  color: var(--color-text-muted);
  margin-bottom: 40px;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.tech-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 40px;
  align-items: center;
}

.tech-item {
  width: 60px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.3s ease;
  filter: grayscale(100%);
  opacity: 0.7;
}

.tech-item:hover {
  filter: grayscale(0%);
  opacity: 1;
  transform: scale(1.2);
}

.tech-icon {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>
