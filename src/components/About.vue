<template>
  <section id="sobre" class="section-with-bg">
    <div class="container">
      <h2>Sobre Mim</h2>
      <div class="sobre-content">
        <img src="/images/profile.jpg" alt="Foto de Pedro Hech" class="profile-img">
        <div class="sobre-texto">
          <p>Olá! Sou Pedro Hech, um profissional apaixonado por tecnologia e inovação, com mais de 7 anos de experiência no desenvolvimento de soluções web escaláveis e sistemas em nuvem.</p>
          <p>Minha expertise combina desenvolvimento full stack com arquitetura de sistemas cloud, criando aplicações robustas e de alto desempenho. Sou certificado em AWS e Google Cloud Platform.</p>
          <p>Quando não estou codando ou projetando arquiteturas de sistemas, você pode me encontrar explorando novas tecnologias, contribuindo para projetos open-source ou praticando trekking nas montanhas.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutComponent'
}
</script>

<style scoped>
.section-with-bg {
  background-color: var(--light-color);
}

.sobre-content {
  display: flex;
  align-items: center;
  gap: 3rem;
}

.profile-img {
  border-radius: 50%;
  border: 5px solid var(--secondary-color);
  width: 200px;
  height: 200px;
  object-fit: cover;
}

.sobre-texto {
  flex: 1;
}

@media (max-width: 768px) {
  .sobre-content {
    flex-direction: column;
    text-align: center;
  }
}
</style>