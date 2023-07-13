<script lang="ts">
	import TopAppBar, { Row, Section, Title } from '@smui/top-app-bar';
	import IconButton from '@smui/icon-button';
	import Button, { Label as ButtonLabel } from '@smui/button';
	import Snackbar, { Label as SnackbarLabel, Actions } from '@smui/snackbar';
	import { createEventDispatcher } from 'svelte';
	import { auth } from '$lib/authStore';
	function handleAuth() {
		$auth = !$auth;
	}

	let snackbar: Snackbar;
	let snackbarText: string;
	const dispatch = createEventDispatcher();

	function toggleDrawer() {
		dispatch('drawer');
	}

	function toggleSnackbar(event: CustomEvent) {
		snackbarText = (event.target as HTMLElement).textContent ?? '';
		snackbar.open();
	}
</script>

<TopAppBar variant="static" color="secondary" prominent={false} dense={false}>
	<Row>
		<Section>
			<IconButton class="material-icons" on:click={toggleDrawer}
				>menu</IconButton
			>
			<Title>Field Management</Title>
		</Section>
		<Section align="end" toolbar>
			<Button variant="raised" on:click={handleAuth}>
				<ButtonLabel>{$auth ? 'Logout' : 'Login'}</ButtonLabel>
			</Button>
			<IconButton on:click={toggleSnackbar} class="material-icons"
				>circle</IconButton
			>
			<IconButton on:click={toggleSnackbar} class="material-icons"
				>login</IconButton
			>
		</Section>
	</Row>
</TopAppBar>

<Snackbar bind:this={snackbar}>
	<SnackbarLabel>Hmm, did you click on the {snackbarText} icon?</SnackbarLabel>
	<Actions>
		<IconButton class="material-icons" title="Dismiss">close</IconButton>
	</Actions>
</Snackbar>
