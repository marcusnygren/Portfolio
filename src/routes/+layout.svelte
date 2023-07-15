<script>
	import { LogoLinkedin } from 'carbon-icons-svelte';
	import '../app.css';
	import 'carbon-components-svelte/css/all.css';
	import { Theme, Button } from 'carbon-components-svelte';
	import WatsonHealthWindowBlackSaturation from 'carbon-icons-svelte/lib/WatsonHealthWindowBlackSaturation.svelte';

	import { LocalStorage, Toggle } from 'carbon-components-svelte';
	import { onMount } from 'svelte';
	import Menu from './menu.svelte';

	let toggled = false;
	let events = [];

	onMount(() => {
		document.documentElement.setAttribute('theme', toggled ? 'g100' : 'g10');
	});

	let theme = 'g100'; // "g10" | "g100"

	const handleClick = () => {
		toggled = !toggled;
		document.documentElement.setAttribute('theme', toggled ? 'g100' : 'g10');
	};
</script>

<LocalStorage
	key="dark-mode"
	bind:value={toggled}
	on:save={() => {
		events = [...events, { event: 'on:save' }];
	}}
	on:update={({ detail }) => {
		events = [...events, { event: 'on:update', detail }];
	}}
/>

<Theme bind:theme persist persistKey="__carbon-theme" />

<Button on:click={handleClick}
	><WatsonHealthWindowBlackSaturation size={32} /><span class="pl-2"
		>Dark mode {toggled ? 'on' : 'off'}</span
	></Button
>

<Menu><slot /></Menu>
