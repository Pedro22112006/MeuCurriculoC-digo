<template>
  <section id="contato" class="section-with-bg">
    <div class="container">
      <h2>Entre em Contato</h2>
      <div class="contato-container">
        <div class="contato-info">
          <h3>Informações de Contato</h3>
          <p><i class="fas fa-envelope"></i> pedro.hech@exemplo.com</p>
          <p><i class="fas fa-phone"></i> (11) 91234-5678</p>
          <p><i class="fas fa-map-marker-alt"></i> Curitiba, PR - Brasil</p>
          
          <div class="social-links">
            <a href="#"><i class="fab fa-linkedin"></i></a>
            <a href="#"><i class="fab fa-github"></i></a>
            <a href="#"><i class="fab fa-twitter"></i></a>
            <a href="#"><i class="fab fa-medium"></i></a>
          </div>
        </div>
        <form class="contato-form" @submit.prevent="submitForm">
          <div class="form-group">
            <input type="text" v-model="form.name" placeholder="Seu Nome" required>
          </div>
          <div class="form-group">
            <input type="email" v-model="form.email" placeholder="Seu E-mail" required>
          </div>
          <div class="form-group">
            <input type="text" v-model="form.subject" placeholder="Assunto">
          </div>
          <div class="form-group">
            <textarea v-model="form.message" placeholder="Sua Mensagem" required></textarea>
          </div>
          <button type="submit" class="btn">Enviar Mensagem</button>
        </form>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContactComponent',
  data() {
    return {
      form: {
        name: '',
        email: '',
        subject: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      console.log('Formulário enviado:', this.form)
      alert('Mensagem enviada com sucesso!')
      this.resetForm()
    },
    resetForm() {
      this.form = {
        name: '',
        email: '',
        subject: '',
        message: ''
      }
    }
  }
}
</script>

<style scoped>
.contato-container {
  display: flex;
  gap: 3rem;
}

.contato-info {
  flex: 1;
  background: white;
  padding: 2rem;
  border-radius: 5px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
}

.contato-info p {
  display: flex;
  align-items: center;
  margin-bottom: 1.5rem;
}

.contato-info i {
  margin-right: 1rem;
  color: var(--secondary-color);
  width: 20px;
  text-align: center;
}

.social-links {
  display: flex;
  gap: 1rem;
  margin-top: 2rem;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 40px;
  height: 40px;
  background: var(--primary-color);
  color: white;
  border-radius: 50%;
  transition: all 0.3s ease;
}

.social-links a:hover {
  background: var(--secondary-color);
  transform: translateY(-3px);
}

.contato-form {
  flex: 1;
  background: white;
  padding: 2rem;
  border-radius: 5px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 5px;
  font-family: inherit;
}

.form-group textarea {
  min-height: 150px;
  resize: vertical;
}

@media (max-width: 768px) {
  .contato-container {
    flex-direction: column;
  }
}
</style>