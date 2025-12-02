<template>
  <div class="landing-page">
    <HeaderSection />
    <HeroSection id="hero" />
    <ValueProposition id="value"/>
    <ServicesSection id="services" />
    <ProcessSection id="process" />
    <TestimonialsSection id="testimonials" />
    <TechStackSection />
    <FaqSection id="faq" />
    <CtaSection id="cta" />
    <FooterSection />
    <ScrollToTop />
  </div>
</template>

<script setup>
import HeaderSection from '../ui/HeaderSection.vue'
import HeroSection from '../ui/HeroSection.vue'
import ValueProposition from '../ui/ValueProposition.vue'
import ServicesSection from '../ui/ServicesSection.vue'
import ProcessSection from '../ui/ProcessSection.vue'
import TestimonialsSection from '../ui/TestimonialsSection.vue'
import TechStackSection from '../ui/TechStackSection.vue'
import FaqSection from '../ui/FaqSection.vue'
import CtaSection from '../ui/CtaSection.vue'
import FooterSection from '../ui/FooterSection.vue'
import ScrollToTop from '../ui/ScrollToTop.vue'
</script>

<style scoped>
.landing-page {
  width: 100%;
  overflow-x: hidden;
}
</style>
