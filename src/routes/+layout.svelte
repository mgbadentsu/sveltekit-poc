<script lang="ts">
	import { AppContent } from '@smui/drawer';
	import AppBar from '$lib/components/AppBar.svelte';
	import Drawer from '$lib/components/Drawer.svelte';

	let open = true;

	function toggleDrawer() {
		open = !open;
	}
</script>

<header>
	<AppBar on:drawer={toggleDrawer} />
</header>
<Drawer bind:open />
<AppContent class="main">
	<main>
		<slot />
	</main>
</AppContent>

<style lang="scss">
	:global(body) {
		margin: 0;
		padding: 0;
	}

	:global(.main) {
		padding-inline: 2rem;
	}
</style>
