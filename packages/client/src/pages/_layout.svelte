<script>
	import { isActive, url, layout } from "@sveltech/routify";

	import Home32 from 'carbon-icons-svelte/lib/Home32';
	import Collaborate32 from 'carbon-icons-svelte/lib/Collaborate32';
	import Folder32 from 'carbon-icons-svelte/lib/Folder32';
	import Calendar32 from 'carbon-icons-svelte/lib/Calendar32';
	import Email32 from 'carbon-icons-svelte/lib/Email32';
	import ChartBar32 from 'carbon-icons-svelte/lib/ChartBar32';

	import NavLink from '../components/ui/NavLink.svelte';
	import Profile from '../components/ui/Profile.svelte'

	const links = [
		['./tab-2', 'Dashboard', Home32],
		['./tab-1', 'Team', Collaborate32],
		['./tab-1', 'Projects', Folder32],
		['./tab-1', 'Calendar', Calendar32],
		['./tab-1', 'Documents', Email32],
		['./tab-1', 'Reports', ChartBar32],
	]
</script>

<div class="h-screen flex overflow-hidden bg-gray-100">
  <div class="flex flex-shrink-0">
    <div class="flex flex-col w-64 border-r border-gray-200 bg-white">
      <div class="h-0 flex-1 flex flex-col pt-5 pb-4 overflow-y-auto">
        <div class="flex items-center flex-shrink-0 px-4">
          <img class="h-8 w-auto" src="/img/logos/workflow-logo-on-white.svg" alt="Workflow" />
        </div>
        <nav class="mt-5 flex-1 px-2 bg-white">
					{#each links as [path, name, Icon]}
						<NavLink link={path} Icon={Icon}>{name}</NavLink>
					{/each}
        </nav>
      </div>
			<Profile />
    </div>
  </div>
  <div class="flex flex-col w-0 flex-1 overflow-hidden">
    <main class="flex-1 relative z-0 overflow-y-auto pt-2 pb-6 focus:outline-none py-6" tabindex="0">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 md:px-8">
        <h1 class="text-2xl font-semibold text-gray-900">Dashboard
        </h1>
      </div>
      <div class="max-w-7xl mx-auto px-4 sm:px-6 md:px-8">
        <slot />
      </div>
    </main>
  </div>
</div>
