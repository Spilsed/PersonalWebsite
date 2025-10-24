<script lang="ts">
	import Card from './Card.svelte';
	import profile from '$lib/assets/profile.png';
	import meras from '$lib/assets/meras.png';
	import { goto } from '$app/navigation';
</script>

<div class="p-4">
	<div class="mr-auto ml-auto max-w-200">
		<div class="mb-5 flex gap-5">
			<img src={profile} alt="Profile" class="overflow-clip rounded-2xl" />
			<div class="px-4">
				<h1 class="text-4xl font-bold">Titan Spellos</h1>
				<p class="mt-5 text-xl">
					Sophomore Computer Science Student at Rensselaer Polytechnic Institute
				</p>
				<div class="flex">
					<button
						class="m-2 ml-0 w-20 cursor-pointer rounded-lg border-2 px-2 transition-all hover:scale-105 hover:shadow-lg"
						onclick={() => window.open('https://www.github.com/Spilsed/')}
					>
						<p class="text-secondary-300 italic">Github</p>
					</button>
					<button
						class="m-2 ml-0 w-20 cursor-pointer rounded-lg border-2 p-2 transition-all hover:scale-105 hover:shadow-lg"
						onclick={() => window.open('https://www.linkedin.com/in/spellos/')}
					>
						<p class="text-secondary-300 italic">LinkedIn</p>
					</button>
					<button
						class="m-2 ml-0 w-20 cursor-pointer rounded-lg border-2 p-2 transition-all hover:scale-105 hover:shadow-lg"
						onclick={() => goto('/blog')}
					>
						<p class="text-secondary-300 italic">Blog</p>
					</button>
				</div>
			</div>
		</div>
		<div class="grid grid-cols-1 gap-2">
			<button
				class="rounded-xl bg-primary-700 p-2 text-center font-bold"
				onclick={() => window.open('https://www.github.com/Spilsed/PerceptronToTransformers')}
			>
				From Perceptron To Transformers
			</button>
		</div>
		<Card title="Meras" img={meras} img_class="h-30 p-3">
			<p class="font-light">
				Meras is a modular calendar app build using Tauri and SvelteKit. The goal is to be
				minimalist and simple, while providing advanced functionality.
			</p>
			<p class="text-xs italic">[In Development]</p>
		</Card>
	</div>
</div>
