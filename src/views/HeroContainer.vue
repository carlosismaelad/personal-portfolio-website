<template>
  <section id="hero-container" class="first-section">
    <div class="hero-container">
      <div class="left-side">
        <div class="header"></div>
        <h1>Carlos Dourado</h1>
        <p>
          Sou um desenvolvedor full stack especializado no desenvolvimento de aplicações escaláveis,
          com foco na entrega de valor através de práticas modernas de software. Combinando
          experiência back-end em Java/Spring boot, Node.js e .NET, serviços em nuvem e habilidades
          front-end em Vue.js e React, desenvolvo soluções abrangentes de ponta a ponta.
        </p>
      </div>
      <div class="right-side">
        <div class="wrap-frame">
          <img
            class="github-image"
            src="https://avatars.githubusercontent.com/u/110005935?s=400&u=2a3b188b9329f4e44d6c25a27661f6f62b55e66a&v=4"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.first-section {
  width: 100%;
  padding: 2rem 1rem;
}

.hero-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
  max-width: 1440px;
  margin: 0 auto;
  padding: 1rem;
}

.left-side,
.right-side {
  width: 100%;
  max-width: 100%;
  text-align: center;
}

/* Reordena os elementos para mobile */
.right-side {
  order: -1;
  margin-top: 3rem;
}

.left-side h1 {
  color: #00ffe9;
  font-size: 2rem;
  font-weight: 600;
  line-height: 1.2em;
  margin-bottom: 1rem;
}

.left-side p {
  color: #ffffff;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.5em;
  margin-bottom: 2rem;
}

.github-image {
  border: 1px solid #00ffe9;
  width: 100%;
  max-width: 20rem;
  height: auto;
  border-radius: 50%;
}

/* Estilos para desktop */
@media (min-width: 768px) {
  .hero-container {
    flex-direction: row;
    gap: 8rem;
    padding-top: 6rem;
    padding-bottom: 80px;
  }

  .left-side,
  .right-side {
    max-width: 50%;
    text-align: left;
  }

  /* Remove a reordenação para desktop */
  .right-side {
    order: 0;
  }

  .left-side h1 {
    font-size: 42px;
  }

  .left-side p {
    font-size: 1.3rem;
  }

  .github-image {
    height: 20rem;
  }
}
</style>
