<script lang="ts">
	import favicon from "$lib/assets/favicon.ico"
	import { FeflowProvider } from "@dxdns/feflow-svelte"

	let { children } = $props()
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<FeflowProvider defaultThemeMode="dark">
	{@render children?.()}
</FeflowProvider>

<style>
	@font-face {
		font-family: "Inter";
		src: url("/fonts/Inter-Regular.woff2") format("woff2");
		font-weight: 400;
		font-style: normal;
		font-display: swap;
	}

	@font-face {
		font-family: "Inter";
		src: url("/fonts/Inter-Bold.woff2") format("woff2");
		font-weight: 700;
		font-style: normal;
		font-display: swap;
	}

	:global(body) {
		font-family: "Inter", sans-serif;
		line-height: 1.2;
		overflow-x: hidden;
	}
</style>
