<script lang="ts">
	type Props = {
		imageSrc: string;
		title: string;
		ingredients: string[];
	};

	let { imageSrc, title, ingredients }: Props = $props();
</script>

<div
	class="mx-auto w-full max-w-md rounded-lg border border-gray-300 bg-green-50 p-6 text-center shadow-lg"
>
	{#if imageSrc}
		<img src={imageSrc} alt={title} class="mb-4 w-full rounded-md object-cover" />
	{/if}
	<h2 class="mb-2 text-3xl font-bold text-orange-700">{title}</h2>
	<p class="mb-4 text-sm text-gray-600 italic">{ingredients.join(', ')}</p>
</div>
