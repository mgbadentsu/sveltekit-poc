<script lang="ts">
	import Paper, { Title, Subtitle, Content } from '@smui/paper';

	export let title = '';
	export let subtitle = '';
	export let variant: Paper['$$prop_def']['variant'] = 'raised';
</script>

<Paper {variant} {...$$restProps}>
	{#if title}
		<Title>{title}</Title>
	{/if}
	{#if subtitle}
		<Subtitle>{subtitle}</Subtitle>
	{/if}
	<Content>
		<slot />
	</Content>
</Paper>
