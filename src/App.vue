<script setup>
import BurgerMenu from './components/BurgerMenu.vue'
import TheHeader from './components/TheHeader.vue'
import HeroContainer from './views/HeroContainer.vue'
import MovingText from './views/MovingText.vue'
import AboutMe from './views/AboutMe.vue'
import Skills from './views/Skills.vue'
import BackToTopButton from './components/BackToTopButton.vue'
import { computed, onMounted, onUnmounted, ref } from 'vue'

// Estado reativo para armazenar a largura da tela
const windowWidth = ref(window.innerWidth)

// Computed para determinar se é mobile
const isMobile = computed(() => windowWidth.value < 768)

// Função para atualizar a largura ao redimensionar a tela
const updateWidth = () => {
  windowWidth.value = window.innerWidth
}

// Adiciona o event listener quando o componente é montado
onMounted(() => {
  window.addEventListener('resize', updateWidth)
})

// Remove o event listener quando o componente é destruído
onUnmounted(() => {
  window.removeEventListener('resize', updateWidth)
})
</script>

<template>
  <div id="app">
    <BurgerMenu v-if="isMobile" />
    <TheHeader v-else />
    <HeroContainer />
    <MovingText />
    <AboutMe />
    <Skills />
    <BackToTopButton />
  </div>
</template>
