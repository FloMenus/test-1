<script>
	export let value;
	export let desc;

	let handleClick = () => {
		value = !value;
	};
</script>

<div>
    <div>
	<p>{desc}</p>
	<input type="checkbox" bind:checked={value} on:click={handleClick} class="toggle toggle-accent"/>
    </div>
	{value}
</div>
