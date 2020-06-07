<script>
	import User32 from 'carbon-icons-svelte/lib/User32';

	export let link;
	export let img;
</script>

<div class="flex-shrink-0 flex border-t border-gray-200 p-4">
	<a href={link} class="flex-shrink-0 group block">
		<div class="flex items-center">
			<div class="h-9 w-9 rounded-full bg-gray-200 flex justify-center items-center">
				{#if img}
					<img
						class="inline-block h-9 w-9 rounded-full"
						src="https://images.unsplash.com/photo-1472099645785-5658abf4ff4e?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80"
						alt="" />
				{:else}
					<User32 />
				{/if}
			</div>
			<div class="ml-3">
				<p
					class="text-sm leading-5 font-medium text-gray-700
					group-hover:text-gray-900">
					Tom Cook
				</p>
				<p
					class="text-xs leading-4 font-medium text-gray-500
					group-hover:text-gray-700 transition ease-in-out duration-150">
					View profile
				</p>
			</div>
		</div>
	</a>
</div>
