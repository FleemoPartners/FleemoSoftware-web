<template>
  <header class="header" :class="{ 'header-scrolled': isScrolled }">
    <div class="container">
      <div class="logo">
        <a href="#" @click.prevent="scrollToSection('hero')">
          <img :src="fleemoLogo" alt="FleemoSoftware Logo" class="logo-img" />
          <span>Fleemo<span class="text-gradient">Software</span></span>
        </a>
      </div>
      
      <nav class="nav-menu" :class="{ 'nav-active': isMenuOpen }">
        <a href="#services" @click.prevent="scrollToSection('services')" class="nav-link">Servicios</a>
        <a href="#process" @click.prevent="scrollToSection('process')" class="nav-link">Proceso</a>
        <a href="#testimonials" @click.prevent="scrollToSection('testimonials')" class="nav-link">Testimonios</a>
        <a href="#faq" @click.prevent="scrollToSection('faq')" class="nav-link">FAQ</a>
        <button class="btn-cta" @click.prevent="scrollToSection('cta')">Cotizar</button>
      </nav>

      <button class="mobile-toggle" @click="toggleMenu">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </button>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import fleemoLogo from '@/assets/fleemo.svg'

const isScrolled = ref(false)
const isMenuOpen = ref(false)

const checkScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const scrollToSection = (id) => {
  isMenuOpen.value = false
  const element = document.getElementById(id)
  if (element) {
    const offset = 80 // Height of header
    const bodyRect = document.body.getBoundingClientRect().top
    const elementRect = element.getBoundingClientRect().top
    const elementPosition = elementRect - bodyRect
    const offsetPosition = elementPosition - offset

    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth'
    })
  }
}

onMounted(() => {
  window.addEventListener('scroll', checkScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', checkScroll)
})
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 1000;
  padding: 20px 0;
  transition: all 0.3s ease;
  background: transparent;
}

.header-scrolled {
  background: rgba(9, 9, 11, 0.8);
  backdrop-filter: blur(12px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  padding: 15px 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo a {
  font-size: 1.5rem;
  font-weight: 800;
  color: var(--color-heading);
  text-decoration: none;
  display: flex;
  align-items: center;
  gap: 10px;
}

.logo-img {
  height: 32px;
  width: auto;
}

.nav-menu {
  display: flex;
  align-items: center;
  gap: 32px;
}

.nav-link {
  color: var(--color-text-muted);
  font-weight: 500;
  font-size: 0.95rem;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: var(--color-primary);
}

.btn-cta {
  background: var(--color-primary);
  color: #000;
  padding: 8px 20px;
  border-radius: 6px;
  font-weight: 600;
  font-size: 0.9rem;
  transition: all 0.3s ease;
}

.btn-cta:hover {
  transform: translateY(-2px);
  box-shadow: 0 0 15px rgba(56, 189, 248, 0.4);
}

.mobile-toggle {
  display: none;
  flex-direction: column;
  gap: 6px;
  background: none;
  border: none;
  cursor: pointer;
}

.bar {
  width: 24px;
  height: 2px;
  background: var(--color-heading);
  transition: 0.3s;
}

@media (max-width: 768px) {
  .mobile-toggle {
    display: flex;
  }

  .nav-menu {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: var(--color-background);
    flex-direction: column;
    padding: 20px;
    border-bottom: 1px solid var(--color-border);
    transform: translateY(-100%);
    opacity: 0;
    pointer-events: none;
    transition: all 0.3s ease;
    z-index: -1;
  }

  .nav-menu.nav-active {
    transform: translateY(0);
    opacity: 1;
    pointer-events: auto;
  }
}
</style>
