<script>

	import { apiData, drinkNames } from './store.js';


		const fetchDrinks = (async () => {
		const response = await fetch('https://www.thecocktaildb.com/api/json/v1/1/filter.php?i=Bourbon')

    return await response.json()

	})()



</script>



{#await fetchDrinks}

	<p>...waiting</p>

	
	
{:then data}
{apiData.set(data)}





{:catch error}
	<p>An error occurred!</p>
{/await}
 
<hr>

<main>
	<h1>DIt moet een andere API zijn...</h1>
<h2>dit hoort ook nog bij de api component</h2>
	<h1>Whiskey Drinks Menu</h1>
	<p>Dit komt weer vanaf een andere api.... </p>
	<ul class="flex">
	{#each $drinkNames as drinkName }
		<div class="test">{drinkName.strDrink} - {drinkName.idDrink} <img src="{drinkName.strDrinkThumb}"  class="images" alt="{drinkName.strDrink}"> </div>

	{/each}



	</ul>
</main>


<hr>

 <style>
	 .flex{display:flex;
	 flex-wrap: wrap;}

	 .images{
		 width: 100px;
	 }

	 .test{
		 display: flex;
		 border:2px solid blue;
	 }

 </style>