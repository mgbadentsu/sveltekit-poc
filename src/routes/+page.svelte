<script lang="ts">
	import Button, { Label } from '@smui/button';
	import PageContent from '$lib/components/PageContent.svelte';
	import { auth } from '$lib/authStore';
	function handleAuth() {
		$auth = !$auth;
	}
</script>

<svelte:head>
	<title>SvelteKit POC</title>
</svelte:head>
<PageContent
	title="This is the home page."
	subtitle="Layout is consistent for all pages below this route level."
>
	<p>
		All content is displayed by using <code>{'<slot />'}</code> blocks. We can easily
		create nested layouts with this approach.
	</p>
	<p>Current auth status: {$auth}</p>
	<Button variant="raised" on:click={handleAuth}>
		<Label>{$auth ? 'Logout' : 'Login'}</Label>
	</Button>
</PageContent>
