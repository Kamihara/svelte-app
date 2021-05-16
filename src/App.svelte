<script>
	let text = 'Svelte';
	let count = 0;
	const handleClickCount = () => count += 1;
	let isActive = false;
	const handleClickActive = () => isActive = !isActive
</script>

<p>Hello {text}!</p>

<p>
	<input type=text bind:value={text}>
</p>

<p>
	<input type=number bind:value={count}>
	<button on:click="{handleClickCount}">+</button>	
</p>

<p>
	<!-- <button on:click="{handleClickActive}" class={isActive ? 'active' : ''}>
		いいね
	</button> -->
	<button on:click="{handleClickActive}" class:active={isActive}>
		いいね
	</button>
</p>

<style>
	.active {
		background-color: #ff3e00;
		color: white;
	}
</style>