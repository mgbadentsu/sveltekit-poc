<script lang="ts">
	import PageContent from '$lib/components/PageContent.svelte';
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
	<p>
		Auth information is saved in a store. We can easily share values in a store
		across the entire application. If you want granular control, you can use
		contexts (and they can be used alongside stores as well).
	</p>
</PageContent>
