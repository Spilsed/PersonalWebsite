<script lang="ts">
	import '../app.css';
	// import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<!-- <link rel="icon" href={favicon} /> -->
</svelte:head>

<div class="h-screen w-screen bg-surface-950 text-white">
	{@render children?.()}
</div>
