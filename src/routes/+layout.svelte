<script lang='ts'>
	// The ordering of these imports is critical to your app working properly
	import '@skeletonlabs/skeleton/themes/theme-rocket.css';
	// If you have source.organizeImports set to true in VSCode, then it will auto change this ordering
	import '@skeletonlabs/skeleton/styles/all.css';
	// Most of your app wide CSS should be put in this file
	import '../app.postcss';

	import { AppShell, AppBar, LightSwitch } from '@skeletonlabs/skeleton';
</script>
<AppShell>
	<svelte:fragment slot="header">
		<AppBar>
			<svelte:fragment slot="lead">
				<a href="/">
					<h3 class="font-bold btn rounded-md">CyberStorm 3</h3>
				</a>
			</svelte:fragment>
			<div class="btn-group mx-auto">
				<a href="/event_info">
					<button class="btn rounded-md variant-ghost-secondary font-bold">
						Event Info
					</button>
				</a>
				<a href="/color_info">
					<button class="btn rounded-md variant-ghost-secondary font-bold">
						What do all the colors mean? 🎨
					</button>
				</a>
			</div>
			<svelte:fragment slot="trail">
				<LightSwitch />
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<slot />
</AppShell>
