<script>
	export let value;
	export let min;
	export let max;

	const handleChange = (e) => {
		if (!isNaN(e.target.value)) {
			// TODO
			if (e.target.value < min) {
				value = min;
			} else if (e.target.value > max) {
				value = max;
			} else {
				value = e.target.value;
			}
			// -------------------------
		}
	};
</script>

<div class="tooltip tooltip-right" data-tip="Max: {max ?? 'none'} |  Min: {min ?? 'none'} ">
	<input
		type="number"
		step="1"
		min={min ?? ''}
		max={max ?? ''}
		bind:value
		class="input input-bordered w-full border-accent"
		on:change={handleChange}
	/>
	{value}
</div>
