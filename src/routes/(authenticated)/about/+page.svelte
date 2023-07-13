<script lang="ts">
	import PageContent from '$lib/components/PageContent.svelte';
</script>

<svelte:head>
	<title>SvelteKit POC - About</title>
</svelte:head>

<PageContent
	title="This is our About page."
	subtitle="We are showcasing the routing capabilities of SvelteKit."
>
	<p>This is a separate route and can have its own layout too.</p>
</PageContent>
