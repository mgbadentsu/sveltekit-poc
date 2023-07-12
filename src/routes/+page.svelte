<script lang="ts">
	import Counter from '$lib/components/Counter.svelte';
	import TopAppBar, { Row, Section, Title } from '@smui/top-app-bar';
	import IconButton from '@smui/icon-button';
</script>

<main>
	<TopAppBar variant="static" color="secondary" prominent={false} dense={false}>
		<Row>
			<Section>
				<IconButton class="material-icons">menu</IconButton>
				<Title>Field Management</Title>
			</Section>
			<Section align="end" toolbar>
				<IconButton class="material-icons">circle</IconButton>
				<IconButton class="material-icons">login</IconButton>
			</Section>
		</Row>
	</TopAppBar>
	<Counter />
</main>

<style lang="scss">
	:global(body) {
		margin: 0;
		padding: 0;
	}
</style>
