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
	class={classNames('popover activation-popover text-sm', className)}
	title="GELU-Aktivierungsfunktion"
	{offset}
	{triggeredBy}
	{trigger}
	{placement}
	arrow={false}
	transition={fade}
	params={{ duration: 0 }}
>
	<div class="activation-content">Entscheidet, ob ein Neuron-Input durchgelassen wird. Dies ist abhängig davon, wie wahrscheinlich er im Kontext der Normalverteilung ist.</div></Popover
>

<style>
	.activation-content {
		width: 10rem;
	}
</style>
