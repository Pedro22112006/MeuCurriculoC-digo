<template>
  <section id="portfolio" class="section-with-bg">
    <div class="container">
      <h2>Portfólio</h2>
      <div class="portfolio-grid">
        <div class="projeto" v-for="project in projects" :key="project.title">
          <img :src="require(`@/images/${project.image}`)" :alt="project.title">
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <a href="#" class="btn">Ver Detalhes</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'PortfolioComponent',
  data() {
    return {
      projects: [
        {
          image: 'project1.jpg',
          title: 'Sistema de Gerenciamento em Nuvem',
          description: 'Plataforma para gerenciamento de recursos em múltiplas clouds com dashboard integrado.'
        },
        {
          image: 'project2.jpg',
          title: 'Aplicativo de Logística',
          description: 'Sistema completo para rastreamento de frota com análise em tempo real.'
        },
        {
          image: 'project3.jpg',
          title: 'Plataforma de Educação',
          description: 'Sistema EAD com videoaulas, exercícios interativos e certificação.'
        }
      ]
    }
  }
}
</script>

<style scoped>
.portfolio-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.projeto {
  background: white;
  border-radius: 5px;
  overflow: hidden;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.projeto:hover {
  transform: translateY(-5px);
}

.projeto img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.projeto h3 {
  padding: 0 1rem;
  margin-top: 1rem;
}

.projeto p {
  padding: 0 1rem;
  color: var(--text-light);
}

.projeto .btn {
  display: block;
  margin: 1rem;
  text-align: center;
}
</style>