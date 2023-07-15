<script lang="ts">
	import { Accordion, AccordionItem } from 'carbon-components-svelte';

	export let link;
	export let name = '';
	export let width = 560;
	export let items = [];

	let innerWidth = 0;
	let innerHeight = 0;

	let gridWidth = 0;

	$: gridWidth = innerWidth / 3;
</script>

<svelte:window bind:innerWidth bind:innerHeight />

<div class="flex justify-between space-x-4 mb-8">
	<div class="flex flex-col justify-between w-full">
		<div class="mb-4">
			<h1 class="text-2xl">{name}</h1>
			<p class="w-[{width}px]"><slot /></p>
		</div>

		<Accordion>
			{#each items as item}
				<AccordionItem title="Awards {items ? '(' + items.length + ')' : ''} & comments">
					{item}
				</AccordionItem>
			{/each}
		</Accordion>
	</div>
	{#if link}
		<div class="w-[{gridWidth}px]">
			<iframe
				width={gridWidth}
				height={gridWidth / 1.777777777777778}
				src={link}
				title="YouTube video player"
				frameborder="0"
				allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
				allowfullscreen
			/>
		</div>
	{/if}
</div>
