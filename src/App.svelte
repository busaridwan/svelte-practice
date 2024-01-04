<script>
	export let firstName;
	let lastName = "Busari";
	$: name = lastName + ' ' + firstName;
	let color = "blue";
	let showText = false;
	const toggle = () => {
		color = color === 'blue' ? 'purple' : 'blue';
		showText = !showText;
		users = [...users, {id: 4, name: 'Baba'}]
	};
	let users = [
		{
			id: 1,
			name: 'Ridwan'
		},
		{
			id: 2,
			name: 'Busari'
		},
		{
			id: 3,
			name: 'Naheem'
		}

	]

</script>

<main>
	<h1 style="color: {color};">Hello {name}!</h1>
	{#if showText}
		<p>Visit the <a href="/">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	{:else}	
	<p>No Text</p>
	{/if}
	
	<button on:click={() => color = 'purple'}>Click</button>
	<button on:click={toggle}>Click</button>
	{#each users as user (user.id) }
		<h3>{user.id}: {user.name}</h3>
	{/each}

</main>

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