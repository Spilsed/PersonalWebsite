<script lang="ts">
	import type { Snippet } from 'svelte';

	const {
		title,
		img,
		img_class,
		children
	}: {
		title: string;
		img?: string;
		img_class?: string;
		children: Snippet;
	} = $props();
</script>

<div class="my-2 flex overflow-clip rounded-xl border-2">
	{#if img}
		<img class={img_class ?? 'h-30'} src={img} alt="Card" />
	{/if}
	<div class="px-2 py-2">
		<h2 class="text-xl font-bold">{title}</h2>
		{@render children?.()}
	</div>
</div>
