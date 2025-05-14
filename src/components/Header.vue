<template>
  <header>
    <div class="container">
      <h1>Pedro Hech</h1>
      <p>Desenvolvedor Full Stack & Especialista em Cloud</p>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent'
}
</script>

<style scoped>
header {
  background: var(--primary-color);
  color: white;
  padding: 2rem 0;
  text-align: center;
}

header h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

header p {
  font-size: 1.2rem;
  opacity: 0.9;
}
</style>