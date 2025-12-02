<template>
  <section class="testimonials-section">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Lo que dicen nuestros <span class="text-gradient">Clientes</span></h2>
        <p class="section-subtitle">Resultados reales de empresas que confiaron en nosotros.</p>
      </div>
      
      <div class="testimonials-grid">
        <div class="testimonial-card" v-for="(item, index) in testimonials" :key="index">
          <div class="quote-icon">“</div>
          <p class="testimonial-text">{{ item.text }}</p>
          <div class="testimonial-author">
            <div class="author-avatar">{{ item.initials }}</div>
            <div class="author-info">
              <h4 class="author-name">{{ item.name }}</h4>
              <p class="author-company">{{ item.company }}</p>
            </div>
          </div>
          <div class="testimonial-result">
            <span>📈 {{ item.result }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    text: "La velocidad de entrega fue impresionante. En 48 horas ya teníamos nuestra landing page lista para recibir tráfico.",
    name: "Carlos Rodríguez",
    company: "TechSolutions",
    initials: "CR",
    result: "Duplicaron nuestros leads"
  },
  {
    text: "El diseño es exactamente lo que buscábamos: moderno, limpio y muy profesional. La atención al detalle es increíble.",
    name: "Ana Martínez",
    company: "Studio Creativo",
    initials: "AM",
    result: "Mejor imagen de marca"
  },
  {
    text: "No solo se ve bien, sino que carga rapidísimo. Hemos notado una mejora significativa en nuestras campañas de Google Ads.",
    name: "Luis García",
    company: "E-commerce X",
    initials: "LG",
    result: "+30% conversión"
  }
]
</script>

<style scoped>
.testimonials-section {
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

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
}

.testimonial-card {
  background: rgba(30, 41, 59, 0.4);
  border: 1px solid rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(10px);
  padding: 30px;
  border-radius: 16px;
  position: relative;
  transition: all 0.3s ease;
}

.testimonial-card:hover {
  transform: translateY(-5px);
  border-color: rgba(56, 189, 248, 0.3);
  box-shadow: 0 10px 30px -10px rgba(0, 0, 0, 0.5);
}

.quote-icon {
  font-size: 4rem;
  color: var(--color-primary);
  line-height: 1;
  position: absolute;
  top: 20px;
  right: 20px;
  font-family: serif;
  opacity: 0.2;
}

.testimonial-text {
  font-size: 1.1rem;
  margin-bottom: 24px;
  position: relative;
  z-index: 1;
  font-style: italic;
  color: var(--color-text);
}

.testimonial-author {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 16px;
}

.author-avatar {
  width: 48px;
  height: 48px;
  background: linear-gradient(135deg, var(--color-primary), #7c3aed);
  color: #fff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  font-size: 1.2rem;
  box-shadow: 0 0 10px rgba(56, 189, 248, 0.3);
}

.author-name {
  font-size: 1rem;
  color: var(--color-heading);
  font-family: var(--font-heading);
}

.author-company {
  font-size: 0.85rem;
  color: var(--color-text-muted);
}

.testimonial-result {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  padding-top: 12px;
  font-size: 0.9rem;
  color: var(--color-primary);
  font-weight: 600;
}
</style>
