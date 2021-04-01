<script>
	import Api from './Api.svelte';
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


</script>

<!-- <button on:click={handleClick}></button> -->
<Test></Test>
	<button on:mouseenter={handleMouseenter}>


	Clicked {count} {count === 1 ? 'time' : 'times'}
	
</button>

<main>
	<h1>Hello {name}!</h1>
	Dit is SVELTE en dit is COOL 👍🏻
	<h1>your age is  <span id="test"> {age	}  </span> !</h1>
</main>

<Api></Api>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
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