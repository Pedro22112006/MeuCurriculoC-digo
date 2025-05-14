<template>
  <section id="habilidades">
    <div class="container">
      <h2>Habilidades</h2>
      <div class="habilidades-grid">
        <div class="habilidade" v-for="skill in skills" :key="skill.title">
          <i :class="skill.icon"></i>
          <h3>{{ skill.title }}</h3>
          <p>{{ skill.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SkillsComponent',
  data() {
    return {
      skills: [
        {
          icon: 'fas fa-code',
          title: 'Desenvolvimento Front-end',
          description: 'React, Angular, Vue.js, TypeScript, HTML5, CSS3'
        },
        {
          icon: 'fas fa-server',
          title: 'Desenvolvimento Back-end',
          description: 'Node.js, Python, Java, Spring Boot, .NET Core'
        },
        {
          icon: 'fas fa-cloud',
          title: 'Cloud Computing',
          description: 'AWS, Google Cloud, Azure, Docker, Kubernetes'
        },
        {
          icon: 'fas fa-database',
          title: 'Banco de Dados',
          description: 'PostgreSQL, MongoDB, Firebase, MySQL, DynamoDB'
        }
      ]
    }
  }
}
</script>

<style scoped>
.habilidades-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.habilidade {
  background: white;
  padding: 2rem;
  border-radius: 5px;
  text-align: center;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}

.habilidade:hover {
  transform: translateY(-10px);
}

.habilidade i {
  font-size: 3rem;
  color: var(--secondary-color);
  margin-bottom: 1rem;
}
</style>