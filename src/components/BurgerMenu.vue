<template>
  <nav id="rolagem">
    <!-- Botão de Abrir Menu -->
    <button
      v-if="!isMenuOpen"
      aria-expanded="false"
      aria-label="Abrir menu"
      @click="openMenu"
      class="menu-button open-menu"
    >
      <svg
        width="40"
        height="40"
        viewBox="0 0 40 40"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M10 20H30"
          stroke="#00856F"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <path
          d="M10 12H30"
          stroke="#00856F"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <path
          d="M18 28L30 28"
          stroke="#00856F"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </button>

    <!-- Botão de Fechar Menu -->
    <button
      v-if="isMenuOpen"
      aria-expanded="true"
      aria-label="Fechar menu"
      @click="closeMenu"
      class="menu-button close-menu"
    >
      <svg
        width="40"
        height="40"
        viewBox="0 0 40 40"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M30 10L10 30M10 10L30 30"
          stroke="#FFFAF1"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </button>

    <!-- Menu de Navegação -->
    <div :class="{ 'menu-open': isMenuOpen }" class="menu">
      <ul>
        <li><a @click="closeMenu" href="#hero-container">Início</a></li>
        <li><a @click="closeMenu" href="#about-me">Sobre</a></li>
        <li><a @click="closeMenu" href="#skills">Skills</a></li>
      </ul>
      <a @click="closeMenu" href="#contact" class="button">Chamar no Whatsapp</a>
    </div>
  </nav>
</template>

<style scoped>
/* Estilos gerais */
nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 72px;
  background: transparent;
  z-index: 100;
  transition: background-color 0.3s ease-in-out; /* Adicionado transição */
}

nav.scroll {
  background-color: #011a17; /* Cor de fundo ao rolar */
}

.menu-button {
  background: none;
  border: none;
  cursor: pointer;
  position: fixed;
  top: 16px;
  right: 16px;
  z-index: 101;
}

/* Menu de Navegação */
.menu {
  position: fixed;
  top: -100%;
  left: 0;
  width: 100%;
  height: 100vh;
  background: #011a17;
  transition: top 0.9s ease-in-out; /* Transição para o topo */
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  z-index: 100;
}

.menu-open {
  top: 0; /* Move o menu para a posição inicial */
}

.menu ul {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 48px;
  text-align: center;
  padding: 0;
  margin: 0;
}

.menu ul li a {
  color: #00ffe9;
  text-decoration: none;
  font-size: 24px;
  font-weight: 700;
}

.menu .button {
  background: #00ffe9;
  color: #011a17;
  text-decoration: none;
  font-size: 18px;
  font-weight: 700;
  text-transform: uppercase;
  padding: 16px 32px;
  border-radius: 40px;
  display: inline-block;
  margin-top: 48px;
}

.menu .button:hover {
  filter: brightness(1.3);
}

/* Estilos para o body quando o menu está expandido */
body.menu-expanded {
  overflow: hidden;
}

body.menu-expanded > :not(nav) {
  visibility: hidden;
}
</style>

<script>
export default {
  data() {
    return {
      isMenuOpen: false,
    }
  },
  methods: {
    openMenu() {
      this.isMenuOpen = true
      document.body.classList.add('menu-expanded')
    },
    closeMenu() {
      this.isMenuOpen = false
      document.body.classList.remove('menu-expanded')
    },
    showNavOnScroll() {
      const nav = document.getElementById('rolagem')
      if (window.scrollY > 0) {
        nav.classList.add('scroll')
      } else {
        nav.classList.remove('scroll')
      }
    },
  },
  mounted() {
    window.addEventListener('scroll', this.showNavOnScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.showNavOnScroll)
  },
}
</script>
