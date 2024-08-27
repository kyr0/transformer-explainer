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
	class={classNames('popover dropout-popover text-sm', className)}
	title="Dropout"
	{offset}
	{triggeredBy}
	{trigger}
	{placement}
	arrow={false}
>
	<div class="dropout-content">Zufällig gewählte Neuronen-Verbindungen werden deaktiviert. Minimiert die Wahrscheinlichkeit für Überanpassung und erhöht die Chance auf Generalisierung.</div></Popover
>
