<script>
	
	const fetchImage = (async () => {
		const response = await fetch('https://dog.ceo/api/breeds/image/random')
    return await response.json()
	})()
</script>



{#await fetchImage}

	<p>...waiting</p>
	
	
	
{:then data}

	<img src={data.message} alt="Dog image" />


{:catch error}
	<p>An error occurred!</p>
{/await}

<h1>Bij elke page refresh krijg je een andere foto van een daggoe</h1>
<h2>dit hoort ook nog bij de api component</h2>