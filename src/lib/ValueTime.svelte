<script>
	export let value;
    export let desc
	let handleChange = (e) => {
		e.preventDefault();
		value = e.target.value;
	};
</script>

<!-- TODO -->
<div>
    <p>{desc}</p>
<input
	type="time"
	bind:value
	class="input input-bordered w-full border-accent"
	on:change={handleChange}
/>
{value}
</div>
<!--      -->
