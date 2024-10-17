<script lang="ts">
    import type { Snippet } from 'svelte';
	import { fade } from 'svelte/transition'

	let { children }: {children: Snippet} = $props()
</script>

<div in:fade={{ duration: 150 }}>{@render children()}</div>