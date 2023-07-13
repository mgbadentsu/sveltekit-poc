<script lang="ts">
	import { page } from '$app/stores';
	import IconButton from '@smui/icon-button';
	import Drawer, { Content, Header, Title, Subtitle } from '@smui/drawer';
	import List, { Item, Text } from '@smui/list';

	export let open = true;

	$: active = $page.url.pathname;
</script>

<Drawer variant="dismissible" bind:open>
	<Header>
		<Title>Field Management</Title>
		<Subtitle>An amazing drawer</Subtitle>
	</Header>
	<Content>
		<List class="drawer-list">
			<Item class="drawer-item" activated={active === '/'} href="/">
				<IconButton class="material-icons">home</IconButton>
				<Text>Home</Text>
			</Item>
			<Item class="drawer-item" activated={active === '/about'} href="/about">
				<IconButton class="material-icons">person</IconButton>
				<Text>About</Text>
			</Item>
			<Item class="drawer-item" activated={active === '/post'} href="/post">
				<IconButton class="material-icons">description</IconButton>
				<Text>Post</Text>
			</Item>
			<Item
				class="drawer-item"
				activated={active === '/reactive'}
				href="/reactive"
			>
				<IconButton class="material-icons">bolt</IconButton>
				<Text>Reactive behavior</Text>
			</Item>
		</List>
	</Content>
</Drawer>

<style lang="scss">
	:global(.drawer-list) {
		display: grid;
		padding-block: 1rem;
	}

	:global(.drawer-item) {
		display: flex;
		align-items: center;
	}
</style>
