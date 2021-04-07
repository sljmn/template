<script>
	import Api_dog_ceo from '../components/Api_dog_ceo.svelte';
	import Api_bol from '../components/Api_bol.svelte';

	

	import Test from './Test.svelte'

	export let name;
	export let age;

	let count = 0;

	function handleMouseenter() {
		// event handler code goes here
		count += 1;
console.log(name)
let test = document.getElementById("test").innerHTML = count

	}
const handleMouseenter1 = () => document.body.style.backgroundColor = "red";
const handleMouseleave = () => document.body.style.backgroundColor = "green";

const handleButtonClick = () => document.body.style.backgroundColor = "#ededed";

</script>

<!-- <button on:click={handleClick}></button> -->

<main>

	<button on:click={handleButtonClick} id="stop">stop de kleuren gekte?</button>

	<Test></Test>
	<button on:mouseenter={handleMouseenter}>


	Clicked {count} {count === 1 ? 'time' : 'times'}
	
</button>
	<Api_bol> </Api_bol>


	<h1>Hello {name}!</h1>
	Dit is SVELTE en dit is COOL 👍🏻
	<h1>your age is  <span id="test"> {age	}  </span> !</h1>

	<Api_dog_ceo></Api_dog_ceo>


</main>


<svelte:body
	on:mouseenter={handleMouseenter1}
	on:mouseleave={handleMouseleave}
/>


<style>

	:global(body) {
		background-color: #ededed;
	}

	main {
		text-align: center;
		padding: 1em;
		width: 540px;
		margin: 0 auto;
		background-color: white;

	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>


