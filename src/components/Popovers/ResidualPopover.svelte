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
	export let reference: PopoverProps['reference'];
</script>

<Popover
	class={classNames('popover residual-popover text-sm', className)}
	title="Residual Connection"
	{offset}
	{triggeredBy}
	{trigger}
	{placement}
	arrow={false}
	transition={fade}
	params={{ duration: 0 }}
	{reference}
>
	<div class="residual-content">
		Adds skip-connections to allow for better gradient flow.
	</div></Popover
>

<style lang="scss">
	:global(.residual-popover) {
		width: 12rem !important;
		.residual-content {
			font-size: 0.8rem;
		}
	}
</style>
