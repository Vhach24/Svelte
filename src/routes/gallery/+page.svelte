<script>
  import Header from '../../components/Header.svelte';
  import Footer from '../../components/Footer.svelte';

  let images = [
    "/espresso.jpg", // Шлях до локального зображення
    "/latte.png",
    "/kava.jpg"
  ];
</script>

<Header />

<main>
  <h2>Галерея</h2>
  <div class="gallery">
    {#each images as image}
      <img src={image} alt="Кава" />
    {/each}
  </div>
</main>

<Footer />

<style>
  main {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    font-family: Arial, sans-serif;
  }
  .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 10px;
  }
  .gallery img {
    width: 200px; /* Встановлюємо фіксовану ширину */
    height: 200px; /* Встановлюємо фіксовану висоту */
    object-fit: cover; /* Зберігаємо пропорції зображення */
    border-radius: 5px;
    transition: transform 0.3s;
  }
  .gallery img:hover {
    transform: scale(1.05); /* Легка анімація при наведенні */
  }
</style>
