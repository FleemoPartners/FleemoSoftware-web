<template>
  <section class="faq-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Preguntas <span class="text-gradient">Frecuentes</span></h2>
        <p class="section-subtitle">Resolvemos tus dudas antes de empezar.</p>
      </div>
      
      <div class="faq-list">
        <div class="faq-item" v-for="(faq, index) in faqs" :key="index" @click="toggleFaq(index)" :class="{ active: activeIndex === index }">
          <div class="faq-question">
            <h3>{{ faq.question }}</h3>
            <span class="faq-icon">+</span>
          </div>
          <div class="faq-answer" v-show="activeIndex === index">
            <p>{{ faq.answer }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const activeIndex = ref(null)

const toggleFaq = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index
}

const faqs = [
  {
    question: '¿Cuánto tarda una landing page?',
    answer: 'Dependiendo del plan, entregamos entre 24 y 72 horas hábiles una vez recibido todo el material necesario.'
  },
  {
    question: '¿Tengo revisiones incluidas?',
    answer: 'Sí, todos nuestros planes incluyen rondas de revisión para asegurar que el resultado final sea exactamente lo que esperas.'
  },
  {
    question: '¿Puedo pedir cambios después de entregada?',
    answer: 'Ofrecemos un periodo de garantía y soporte post-entrega. Para cambios mayores después de este periodo, tenemos tarifas preferenciales.'
  },
  {
    question: '¿Incluye dominio y hosting?',
    answer: 'El Plan Empresa incluye configuración de hosting y dominio. En los otros planes, te asesoramos para contratarlos a tu nombre (recomendado para que seas el dueño total).'
  },
  {
    question: '¿Puedo elegir el diseño?',
    answer: '¡Por supuesto! No usamos plantillas rígidas. Adaptamos el diseño a tu marca, colores y preferencias visuales.'
  }
]
</script>

<style scoped>
.faq-section {
  padding: var(--section-gap) 20px;
  position: relative;
}

.container {
  max-width: 800px;
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

.faq-list {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

.faq-item {
  background: rgba(30, 41, 59, 0.4);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 8px;
  overflow: hidden;
  transition: all 0.3s ease;
  cursor: pointer;
}

.faq-item:hover {
  border-color: rgba(56, 189, 248, 0.3);
  background: rgba(30, 41, 59, 0.6);
}

.faq-item.active {
  border-color: var(--color-primary);
  background: rgba(30, 41, 59, 0.8);
  box-shadow: 0 0 20px rgba(56, 189, 248, 0.1);
}

.faq-question {
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.faq-question h3 {
  font-size: 1.1rem;
  margin: 0;
  font-weight: 500;
  font-family: var(--font-heading);
}

.faq-icon {
  font-size: 1.5rem;
  color: var(--color-primary);
  transition: transform 0.3s ease;
}

.faq-item.active .faq-icon {
  transform: rotate(45deg);
}

.faq-answer {
  padding: 0 20px 20px;
  color: var(--color-text-muted);
  line-height: 1.6;
  animation: slideDown 0.3s ease;
}

@keyframes slideDown {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>
