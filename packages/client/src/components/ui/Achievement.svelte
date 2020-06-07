<script>
	import TrophyFilled32 from 'carbon-icons-svelte/lib/TrophyFilled32';

	export let text;
	export let link;
</script>

<!-- TODO:: Think about Animation -->

<div class="fixed bottom-0 right-0 left-0 flex justify-center pb-3">
	<div class="flex rounded-full bg-green-600 w-96">
		<div
			class="rounded-full h-14 w-14 bg-green-400 flex items-center
			justify-center">
			<TrophyFilled32 class="text-white fill-current" />
		</div>
		<div class="flex-1 flex justify-between items-center p-3">
			<p class="text-sm text-white">{text}</p>
			<p class="text-sm leading-5 text-small">
				<a
					href={link}
					class="whitespace-no-wrap font-medium text-white hover:text-blue-200
					transition ease-in-out duration-150">
					Details &rarr;
				</a>
			</p>
		</div>
	</div>
</div>
