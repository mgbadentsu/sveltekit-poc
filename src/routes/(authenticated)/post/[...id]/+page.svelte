<script lang="ts">
	import { page } from '$app/stores';
	import PageContent from '$lib/components/PageContent.svelte';
</script>

<PageContent class="post" variant="raised">
	<p>This is the output of the current route. Pretty neat, huh?</p>
	<p>You are now viewing the {$page.route.id} route</p>
	<p>Your current path is {$page.url.pathname}</p>
</PageContent>

<style lang="scss">
	:global(.post) {
		background-color: #ff3e00 !important;
	}
</style>
