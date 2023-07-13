<script lang="ts">
	import { goto } from '$app/navigation';
	import Textfield from '@smui/textfield';
	import Button, { Label } from '@smui/button';
	let value = '';

	function handleClick() {
		goto(`/post/${value}`);
	}
</script>

<svelte:head>
	<title>SvelteKit POC - Post</title>
</svelte:head>

<Textfield bind:value label="URL" variant="outlined" />
<Button on:click={handleClick} disabled={!value} variant="raised">
	<Label>Navigate</Label>
</Button>
