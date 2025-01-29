<template>
  <section class="second-section">
    <h2 class="background-moving-text-blue">
      Full stack * Back end * Node.js * .NET * Javascript * Java * Spring boot * Ruby * Ruby on
      Rails * Front end * Vue.js * React * Angular
    </h2>
    <h2 class="background-moving-text-white">
      Full stack * Back end * Node.js * .NET * Javascript * Java * Spring boot * Ruby * Ruby on
      Rails * Front end * Vue.js * React * Angular
    </h2>
  </section>
</template>

<style>
.second-section {
  position: relative;
  overflow: hidden;
  padding-top: 1.5rem;
  min-height: 10rem;
  display: flex;
  align-items: center;
  flex-direction: column;
  gap: 0.5rem;
}

.background-moving-text-white,
.background-moving-text-blue {
  text-align: center;
  color: #ffffff;
  font-size: 36px;
  font-weight: 600;
  line-height: 1.2em;
  white-space: nowrap;
  overflow: hidden;
}
.background-moving-text-blue {
  color: #00ffe9;
}
</style>
<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

export default {
  name: 'AnimatedText',
  mounted() {
    // Registrar o plugin ScrollTrigger
    gsap.registerPlugin(ScrollTrigger)

    // Animação para background-moving-text-blue
    let backgroundMovingTextBlue = gsap.timeline({
      scrollTrigger: {
        trigger: '.background-moving-text-blue',
        start: 'bottom 80%',
        end: 'bottom 20%',
        scrub: 2,
        markers: false,
      },
    })

    backgroundMovingTextBlue.to(
      '.background-moving-text-blue',
      {
        transform: 'translateX(-15%)',
      },
      'animation-text',
    )

    // Animação para background-moving-text-white
    let backgroundMovingTextWhite = gsap.timeline({
      scrollTrigger: {
        trigger: '.background-moving-text-white',
        start: 'bottom 90%',
        end: 'bottom 10%',
        scrub: 2,
        markers: false,
      },
    })

    backgroundMovingTextWhite.to(
      '.background-moving-text-white',
      {
        transform: 'translateX(15%)',
      },
      'animation-text',
    )
  },
}
</script>
