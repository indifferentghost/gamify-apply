<script>
	import { isActive } from '@sveltech/routify'
	import clsx from 'clsx';

	export let link;
	export let Icon;
</script>

<a href={link} class={clsx('group flex items-center px-2 py-2 text-sm leading-6 font-medium text-gray-900 rounded-md focus:outline-none focus:bg-gray-200 transition ease-in-out duration-150', {'bg-gray-100': $isActive(link)} )}>
	<svelte:component this={Icon} class="mr-4 h-6 w-6 text-gray-500 group-hover:text-gray-500 group-focus:text-gray-600 transition ease-in-out duration-150" fill="none" viewBox="0 0 24 24" stroke="currentColor" />
	<slot />
</a>
