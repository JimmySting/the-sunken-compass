<script lang="ts">
	import { base } from '$app/paths';
	import DrinkMenuItem from '$lib/components/DrinkMenuItem.svelte';

	type Drink = {
		id: number;
		imageSrc: string;
		title: string;
		ingredients: string[];
	};

	// Drink data
	const menuItems: Drink[] = [
		{
			id: 1,
			imageSrc: `${base}/img/daiquiri.png`,
			title: 'House Daiquiri',
			ingredients: ['Probitas', 'Kohana Kea', 'Midori', 'Lime', 'Simple', 'Chartreuse']
		},
		{
			id: 2,
			imageSrc: `${base}/img/old-fashioned.png`,
			title: 'Rum Old Fashioned',
			ingredients: ['El Dorado 12', 'Allspice', 'Simple', 'Bitters']
		},
		{
			id: 3,
			imageSrc: `${base}/img/fifty-fifty.png`,
			title: 'Fifty-Fifty',
			ingredients: ['Smith & Cross', 'Cynar']
		},
		{
			id: 4,
			imageSrc: `${base}/img/beerlao.png`,
			title: 'House Beer',
			ingredients: ['Laotian gold!']
		}
	];
</script>

<div class="min-h-screen bg-gradient-to-br from-slate-700 via-slate-800 to-slate-900 px-4 py-10">
	<header class="mb-12 text-center">
		<h1
			class="text-5xl font-bold tracking-tight text-white md:text-6xl"
			style="font-family: 'Lobster', cursive;"
		>
			The Sunken Compass
		</h1>
		<p class="mt-2 text-xl text-yellow-300">Good vibes, mysterious tides</p>
	</header>

	<main class="flex flex-col items-center space-y-10">
		{#each menuItems as item (item.id)}
			<DrinkMenuItem imageSrc={item.imageSrc} title={item.title} ingredients={item.ingredients} />
		{/each}
	</main>

	<footer class="mt-16 py-6 text-center">
		<p class="text-opacity-90 text-sm text-white">Sip responsibly and enjoy the vibes!</p>
	</footer>
</div>
