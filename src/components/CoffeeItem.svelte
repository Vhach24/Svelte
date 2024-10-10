<!-- src/components/CoffeeItem.svelte -->
<script>
  export let coffee; // Приймаємо об'єкт кави як пропс
</script>

<div class="coffee-item">
  <h3>{coffee.name}</h3>
  <img src={coffee.image} alt={coffee.name} />
  <p>{coffee.description}</p>
  <p>Ціна: <strong>{coffee.price} грн</strong></p>
</div>

<style>
  .coffee-item {
    border: 1px solid #ccc;
    border-radius: 8px;
    padding: 15px;
    margin: 10px;
    text-align: center;
    background-color: #f9f9f9;
    transition: transform 0.3s;
  }
  .coffee-item:hover {
    transform: translateY(-5px); /* Легка анімація при наведенні */
  }
  .coffee-item img {
    max-width: 100%;
    height: auto;
    border-radius: 8px;
  }
</style>
