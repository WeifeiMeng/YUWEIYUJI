<template>
  <div class="app">
    <HeroSection />
    <BrandStrategy />
    <BrandStory />
    <BrandValues />
    <BrandPersonality />
    <UserProfile />
    <VisualSystem />
    <ProductStrategy />
    <BrandLanguage />
    <ContentChannel />
    <FuturePlan />
    <EcommerceSpec />
    <ClosingSection />
    <PrintButton />
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import HeroSection from './components/HeroSection.vue'
import BrandStrategy from './components/BrandStrategy.vue'
import BrandStory from './components/BrandStory.vue'
import BrandValues from './components/BrandValues.vue'
import BrandPersonality from './components/BrandPersonality.vue'
import UserProfile from './components/UserProfile.vue'
import VisualSystem from './components/VisualSystem.vue'
import ProductStrategy from './components/ProductStrategy.vue'
import BrandLanguage from './components/BrandLanguage.vue'
import ContentChannel from './components/ContentChannel.vue'
import FuturePlan from './components/FuturePlan.vue'
import EcommerceSpec from './components/EcommerceSpec.vue'
import ClosingSection from './components/ClosingSection.vue'
import PrintButton from './components/PrintButton.vue'

onMounted(() => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible')
      }
    })
  }, { threshold: 0.12, rootMargin: '0px 0px -40px 0px' })

  document.querySelectorAll('.fade-in').forEach(el => observer.observe(el))
})
</script>
