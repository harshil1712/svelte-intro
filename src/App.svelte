<script>
  import svelteLogo from './assets/svelte.svg'
  import Counter from './lib/Counter.svelte'
  import Card from './lib/Card.svelte'
  import {hasVat} from './lib/store'
  const data = [{
    title: "Prodcut 1",
    description: "This is a product you can buy only here",
    price: 30,
  },
  {
    title: "Prodcut 2",
    description: "This is a product you can buy only here",
    price: 60,
  },
  {
    title: "Prodcut 3",
    description: "This is a product you can buy only here",
    price: 10,
  }]
</script>

<main>
  <h1>Vite + Svelte</h1>
  <div>
    {#each data as item}
		<Card title={item.title} description={item.description} price={item.price} />
	{/each}
  </div>
</main>

<style global>
  @import "https://unpkg.com/open-props";
  @import "https://unpkg.com/open-props/normalize.min.css";

</style>
