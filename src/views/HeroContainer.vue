<template>
  <section id="home" class="first-section">
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

<style>
.first-section {
  width: 100%;
  height: 100%;
  gap: 10rem;
}

.hero-container {
  display: flex;
  max-width: 1440px;
  margin-inline: auto;
  align-items: center;
  padding-top: 6rem;
  gap: 8rem;
  justify-content: center;
  padding-bottom: 80px;
}

.left-side,
.right-side {
  max-width: 50%;
  z-index: 3;
}

.left-side h1 {
  color: #00ffe9;
  font-size: 42px;
  font-weight: 600;
  line-height: 1.2em;
  margin-bottom: 20px;
  max-width: 500px;
}
.left-side p {
  color: #ffffff;
  padding-top: 1.5rem;
  font-size: 1.3rem;
  font-weight: 600;
  line-height: 1.2em;
  text-align: left;
  margin-bottom: 80px;
  max-width: 475px;
  line-height: 1.2em;
}

.github-image {
  border: 1px solid #00ffe9;
  height: 20rem;
  border-radius: 50%;
  overflow: hidden;
}
</style>
