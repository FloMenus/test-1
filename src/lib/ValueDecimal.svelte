<script>
	export let value;
	export let min;
	export let max;
	export let precision;


	const handleChange = (e) => {
		e.preventDefault();
		// TODO
		if (e.target.value < min) {
			value = min;
		} else if (e.target.value > max) {
			value = max;
		} else if (e.target.value.toString().length > precision + 2) {
			value = value.toFixed(precision);
		} else {
			value = e.target.value;
		}
		// -------------------------
	};
</script>

<div
	class="tooltip tooltip-right"
	data-tip="Max: {max ?? 'none'} |  Min: {min ?? 'none'} | Precision: {precision ?? 'none'}"
>
	<input
		type="number"
		step="0.1"
		min={min ?? ''}
		max={max ?? ''}
		bind:value
		class="input input-bordered w-full border-accent"
		on:change={handleChange}
	/>
	{value}
	<!--         -->
</div>
