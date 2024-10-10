<script>
  import Header from '../../components/Header.svelte';
  import Footer from '../../components/Footer.svelte';
  import CoffeeItem from '../../components/CoffeeItem.svelte';

  // Список кав
  let coffees = [
    {
      name: "Еспресо",
      image: "/espresso.jpg",
      description: "Класичний еспресо з насиченим смаком.",
      price: 40
    },
    {
      name: "Латте",
      image: "/latte.png",
      description: "М'який латте з молоком.",
      price: 50
    },
    {
      name: "Капучино",
      image: "/cappuccino.jpg",
      description: "Капучино з молочною піною.",
      price: 55
    }
  ];
</script>

<Header />

<main>
  <h2>Меню</h2>
  <div class="coffee-list">
    {#each coffees as coffee}
      <CoffeeItem {coffee} />
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
  .coffee-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
  }
</style>
