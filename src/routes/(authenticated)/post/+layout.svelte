<script lang="ts">
	import PageContent from '$lib/components/PageContent.svelte';
</script>

<PageContent
	title="This is our Posts page."
	subtitle="Hey! We have a different layout"
	variant="unelevated"
>
	<p>Try appending <code>{'/anything/you/want'}</code> to the url</p>
	<slot />
</PageContent>
