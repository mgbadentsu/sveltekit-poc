<script lang="ts">
	import Button, { Label } from '@smui/button';
	let count = 0;
	let isEnabled = false;

	function enableCounter() {
		isEnabled = !isEnabled;
	}
	function increment() {
		count = count + 1;
	}

	function decrement() {
		count = count > 0 ? count - 1 : count;
	}
</script>

<section class="Counter">
	<Button on:click={enableCounter} variant="raised">
		<Label>Enable counter component</Label>
	</Button>
	{#if isEnabled}
		<p class="Counter__text">{count}</p>
		<div class="Counter__actions">
			<Button on:click={increment} variant="raised">
				<Label>+</Label>
			</Button>
			<Button on:click={decrement} variant="raised">
				<Label>-</Label>
			</Button>
		</div>
	{/if}
</section>

<style lang="scss">
	.Counter {
		display: grid;
		column-gap: 1rem;
		align-items: center;
		justify-content: center;

		.Counter__text {
			border: 1px solid black;
			border-radius: 5px;
			padding-inline: 1rem;
			background-color: white;
			color: black;
			font-size: 1.25rem;
			text-align: center;
		}
	}
</style>
