<script lang="ts">
	import classNames from 'classnames';
	import { Popover } from 'flowbite-svelte';
	import type { PopoverProps } from 'flowbite-svelte/Popover.svelte';
	import { fade } from 'svelte/transition';

	export let offset: PopoverProps['offset'] = undefined;
	export let className: PopoverProps['class'] = undefined;
	export let triggeredBy: PopoverProps['triggeredBy'] = undefined;
	export let trigger: PopoverProps['trigger'] = 'hover';
	export let placement: PopoverProps['placement'] = 'right';
</script>

<Popover
	class={classNames('popover ln-popover text-sm', className)}
	title="Normalisierung der Eingabevektoren pro Schicht"
	{offset}
	{triggeredBy}
	{trigger}
	{placement}
	arrow={false}
	transition={fade}
	params={{ duration: 0 }}
>
	<div class="ln-content w-[10rem]">
		Standardisiert die Eingabevektoren<br />
		jeder Schicht auf eine Normalverteilung.<br />
		Dabei werden die Mittelwerte und <br />
		Varianzen aller <br />Vektoren <br />
		vereinheitlicht.
	</div></Popover
>
