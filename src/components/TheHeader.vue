<template>
  <header>
    <div class="nav-container">
      <button>
        <a href="#home">Home</a>
      </button>
      <button>
        <a href="#about-me">Sobre</a>
      </button>
      <button>
        <a href="#projects">Projetos</a>
      </button>
      <button>
        <a href="#contacts">Contatos</a>
      </button>
    </div>
  </header>
</template>

<style scoped>
.nav-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 4rem;
  margin-top: 1rem;
  gap: 4rem;
}
button {
  background-color: transparent;
  border: none;
  font-size: 1.2rem;

  a {
    color: #00ffe9;
    text-decoration: none;
  }
}
</style>
