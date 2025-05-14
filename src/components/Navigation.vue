<template>
  <nav>
    <div class="container">
      <ul>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#habilidades">Habilidades</a></li>
        <li><a href="#portfolio">Portfólio</a></li>
        <li><a href="#experiencia">Experiência</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'NavigationComponent'
}
</script>

<style scoped>
nav {
  background: var(--dark-color);
  position: sticky;
  top: 0;
  z-index: 100;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

nav ul {
  display: flex;
  justify-content: center;
  list-style: none;
}

nav ul li a {
  color: white;
  padding: 1rem 1.5rem;
  display: block;
  transition: all 0.3s ease;
}

nav ul li a:hover {
  background: var(--secondary-color);
  color: white;
}

@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    text-align: center;
  }
}
</style>