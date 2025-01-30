<template>
  <section id="about-me" class="about-me">
    <p class="text">
      Como um bom programador pragmático, priorizo a entrega iterativa, equilibrando desempenho e
      qualidade, evitando excesso de engenharia. Meu compromisso com as melhores práticas, como
      testes e arquiteturas resilientes, garante sistemas sustentáveis, escaláveis e confiáveis.
    </p>
  </section>
</template>

<style scoped>
.about-me {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
  padding: 1.5rem;
  width: 100%;
  max-width: 80%;
  margin: 2rem auto;
  background-color: #000000;
  border: 1px solid #00ffe9;
  border-radius: 2rem;
  overflow: hidden;
}

.text {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 6rem;
  width: 100%;
  max-width: 100%;
  margin: 0 auto;
  padding: 1.5rem;
  text-align: center;
  color: #ffffff;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.5em;
  overflow: hidden;
}

/* Estilos para desktop */
@media (min-width: 768px) {
  .about-me {
    margin-top: 4rem;
    margin-bottom: 4rem;
  }

  .text {
    min-height: 8rem;
    max-width: 80rem;
    font-size: 1.2rem;
    padding: 2rem;
  }
}
</style>
