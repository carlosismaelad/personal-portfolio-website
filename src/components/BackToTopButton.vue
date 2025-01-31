<template>
  <a id="backToTopButton" @click="scrollToTop">
    <svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
      <circle cx="20" cy="20" r="20" fill="#00856F" />
      <path
        d="M20 27V13"
        stroke="white"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
      <path
        d="M13 20L20 13L27 20"
        stroke="white"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </svg>
  </a>
</template>

<style scoped>
#backToTopButton circle {
  fill: #011a17;
}

#backToTopButton {
  position: fixed;
  bottom: 1rem;
  right: 2.5rem;
  opacity: 0;
  visibility: hidden;
  transform: translateY(150%);
  transition: 200ms;
}

#backToTopButton.show {
  opacity: 1;
  visibility: visible;
  transform: translateY(0%);
}
</style>

<script>
export default {
  mounted() {
    window.addEventListener('scroll', this.showBackToTopButtonOnScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.showBackToTopButtonOnScroll)
  },
  methods: {
    showBackToTopButtonOnScroll() {
      const backToTopButton = document.getElementById('backToTopButton')
      if (window.scrollY > 400) {
        backToTopButton.classList.add('show')
      } else {
        backToTopButton.classList.remove('show')
      }
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth', // Rolagem suave
      })
    },
  },
}
</script>
