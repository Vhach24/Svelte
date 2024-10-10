<!-- src/components/Header.svelte -->
<script>
  export let title = 'Кав\'ярня'; // Назва кав'ярні
</script>

<header>
  <h1>{title}</h1>
  <nav>
    <a href="/">Головна</a>
    <a href="/menu">Меню</a>
    <a href="/gallery">Галерея</a>
   
  </nav>
</header>

<style>
  header {
    background-color: #8B4513; /* Коричневий колір */
    color: white;
    padding: 20px;
    text-align: center;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  }
  nav a {
    color: white;
    margin: 0 15px;
    text-decoration: none;
    transition: color 0.3s;
  }
  nav a:hover {
    color: #FFD700; /* Золотий колір */
  }
</style>
