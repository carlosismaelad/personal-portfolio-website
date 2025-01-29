<template>
  <section class="skills-section">
    <div class="title">Principais competências e tecnologias:</div>
    <div class="skills-content">
      <h3>Back-end:</h3>
      <ul>
        <li>
          Node.js, Ruby e Ruby on Rails, Spring boot, Spring security, ASP.NET Core e ASP.NET
          Framework, JUnity, xUnity
        </li>
      </ul>
      <h3>Front-end:</h3>
      <ul>
        <li>
          Vue.js, React, TypeScript, JavaScript (ES6+), TailwindCSS, HTML5, CSS3, SASS/SCSS,
          Angularjs
        </li>
      </ul>
      <h3>Bancos de dados:</h3>
      <ul>
        <li>PostgreSQL, SQL Server</li>
      </ul>
      <h3>Arquitetura e Design:</h3>
      <ul>
        <li>Clean Architecture, Domain Driven Design (DDD), Arquitetura hexagonal</li>
      </ul>
      <h3>Serviços e ferramentas em nuvem:</h3>
      <ul>
        <li>
          Azure DevOps, AWS EC2, AWS S3, AWS SES, CI/CD pipelines, Prisma, IntelliJ, Visual Studio,
          VsCode
        </li>
      </ul>
    </div>
  </section>
</template>

<style>
.skills-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.5rem;
  padding: 1.5rem;
  max-width: 80rem;
  margin: 0 auto;
  background-color: #000000;
  border: 1px solid #00ffe9;
  border-radius: 2rem;
  overflow: hidden;
  margin-bottom: 6rem;
}

.title {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  color: #ffffff;
  font-size: 1.5rem;
  font-weight: 600;
  line-height: 1.2em;
}

.skills-content {
  color: #ffffff;
  font-size: 1rem;
  line-height: 1.5em;
  padding: 0 1.5rem;
}

.skills-content h3 {
  color: #00ffe9;
  font-size: 1.2rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
}

.skills-content ul {
  padding-left: 1.5rem;
  margin-bottom: 1rem;
}

.skills-content li {
  margin-bottom: 0.5rem;
}
</style>
