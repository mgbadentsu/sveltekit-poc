<script lang="ts">
	import Paper, { Content } from '@smui/paper';
	import Textfield from '@smui/textfield';

	let value = '';
</script>

<Paper>
	<Content>
		<p>
			If you type anything in the textarea below you'll get instant feedback.
		</p>
		<p>
			No useEffect, no useState. And we can also iterate over the text, split
			new lines with amazing svelte directives.
		</p>
		<p>Pretty easy huh?</p>
		<Textfield textarea label="Text" bind:value />
		<br />
		<code>
			{#each value.split('\n') as line}
				{line}
				<br />
			{/each}
		</code>
	</Content>
</Paper>

<style lang="scss">
</style>
