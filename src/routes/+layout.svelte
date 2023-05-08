<script>
	import { setContext } from 'svelte';
	import { writable } from 'svelte/store';
	import { RadioStatic } from 'radio-color-system';

	import '$utils/_variables.scss';

	let colors = writable([
		{
			color: { h: 240, s: 32, l: 48 },
			name: ['primary', 'secondary', 'tertiary']
		},
		{ color: { h: 270, s: 2, l: 57 }, name: 'neutral' }
	]);

	setContext('colors', colors);
</script>

<RadioStatic colors={$colors} async={true} />

<slot />
