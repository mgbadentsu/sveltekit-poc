<script lang="ts">
	import PageContent from '$lib/components/PageContent.svelte';
</script>

<PageContent
	title="This is our Posts page."
	subtitle="Hey! We have a different layout"
	variant="unelevated"
>
	<p>
		Try tryping <code>{'/anything/you/want'}</code> in the textfield, then click
		the navigate button
	</p>
	<slot />
</PageContent>
