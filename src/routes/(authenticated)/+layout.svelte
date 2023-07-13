<script lang="ts">
	import { auth } from '$lib/authStore';
</script>

{#if $auth}
	<slot />
{:else}
	<p>Please login</p>
{/if}
