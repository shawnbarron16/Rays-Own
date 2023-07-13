<script lang="ts">
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-vintage.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/skeleton.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
</script>

<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/5 w-56 p-4">
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar gridColumns="grid-cols-3" slotDefault="place-self-center" slotTrail="place-content-end">
			<svelte:fragment slot="lead">
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/"
					target="_blank"
					rel="noreferrer"
				>
					Home
				</a>
			</svelte:fragment>
			<svelte:fragment slot="default">
				<strong class="h1 uppercase">Rays Own</strong>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/aboutus"
					target="_blank"
					rel="noreferrer"
				>
					About Us
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/bbq"
					target="_blank"
					rel="noreferrer"
				>
					BBQ Service
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/contact"
					target="_blank"
					rel="noreferrer"
				>
					Contact Us
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/news"
					target="_blank"
					rel="noreferrer"
				>
					Ray's News Letter
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/recipes"
					target="_blank"
					rel="noreferrer"
				>
					Recipes
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="/testimonials"
					target="_blank"
					rel="noreferrer"
				>
					Testimonials
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>

	<svelte:fragment slot="sidebarLeft">
		<!-- Insert the list: -->
		<nav class="list-nav">
			<ul>
				<li><a href="/jerkey-types">Jerkey Types</a></li>
				<li><a href="/sausage-types">Sausage Types</a></li>
				<li><a href="/spices">Dredge & Spices</a></li>
				<li><a href="/gifts">Gift Boxes</a></li>
			</ul>
		</nav>
		<!-- --- -->
	</svelte:fragment>

	<!-- Page Route Content -->
	<slot />
</AppShell>
