<template>
  <section id="experiencia">
    <div class="container">
      <h2>Experiência Profissional</h2>
      <div class="timeline">
        <div class="timeline-item" v-for="(exp, index) in experiences" :key="index" 
             :class="{ 'left': index % 2 === 0, 'right': index % 2 !== 0 }">
          <div class="timeline-content">
            <h3>{{ exp.company }}</h3>
            <p class="timeline-date">{{ exp.period }}</p>
            <p class="timeline-position">{{ exp.position }}</p>
            <p>{{ exp.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ExperienceComponent',
  data() {
    return {
      experiences: [
        {
          company: 'CloudTech Solutions',
          period: '2021 - Presente',
          position: 'Arquiteto de Soluções Cloud',
          description: 'Liderança de projetos de migração para nuvem e desenvolvimento de arquiteturas escaláveis. Responsável por treinamentos e certificações da equipe.'
        },
        {
          company: 'Digital Innovation Ltda.',
          period: '2018 - 2021',
          position: 'Desenvolvedor Sênior Full Stack',
          description: 'Desenvolvimento de aplicações web complexas e APIs RESTful. Implementação de CI/CD e práticas DevOps.'
        },
        {
          company: 'TechStart Consultoria',
          period: '2015 - 2018',
          position: 'Desenvolvedor Back-end',
          description: 'Desenvolvimento de sistemas corporativos e integração com bancos de dados relacionais e não-relacionais.'
        }
      ]
    }
  }
}
</script>

<style scoped>
.timeline {
  position: relative;
  max-width: 800px;
  margin: 0 auto;
}

.timeline::before {
  content: '';
  position: absolute;
  width: 2px;
  background-color: var(--secondary-color);
  top: 0;
  bottom: 0;
  left: 50%;
  margin-left: -1px;
}

.timeline-item {
  padding: 10px 40px;
  position: relative;
  width: 50%;
  box-sizing: border-box;
}

.timeline-item.left {
  left: 0;
}

.timeline-item.right {
  left: 50%;
}

.timeline-content {
  padding: 20px;
  background: white;
  border-radius: 5px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
}

.timeline-item::after {
  content: '';
  position: absolute;
  width: 20px;
  height: 20px;
  background-color: white;
  border: 4px solid var(--secondary-color);
  border-radius: 50%;
  top: 15px;
  z-index: 1;
}

.timeline-item.left::after {
  right: -10px;
}

.timeline-item.right::after {
  left: -10px;
}

.timeline-date {
  color: var(--secondary-color);
  font-weight: bold;
}

.timeline-position {
  font-weight: bold;
  margin-bottom: 0.5rem;
}

@media (max-width: 768px) {
  .timeline::before {
    left: 31px;
  }
  
  .timeline-item {
    width: 100%;
    padding-left: 70px;
    padding-right: 25px;
  }
  
  .timeline-item.right {
    left: 0;
  }
  
  .timeline-item::after {
    left: 21px;
  }
  
  .timeline-item.left::after,
  .timeline-item.right::after {
    left: 21px;
  }
}
</style>