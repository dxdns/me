<script lang="ts">
	import { Avatar, Card, Link } from "@dxdns-kit/svelte"
	import profileImage from "$lib/assets/profile.jpeg"

	let { data } = $props()
</script>

<svelte:head>
	<title>me | {data.title}</title>
</svelte:head>

<div
	style="
    line-height: 1.5;
    display: flex;
    align-items: center;
    justify-content: center;
	height: 100vh;
    "
>
	<Card
		animatedBorder
		style="
		display: flex;
		align-items: center;
		flex-direction: column;
		padding: 3rem;
		border-radius: 16px;
		text-align: center;
		"
	>
		<div class="rounded-full gradient-border">
			<Avatar
				alt="profile"
				textFallback="Diógenes Rodrigues"
				src={profileImage}
				height="175px"
				width="175px"
			/>
		</div>
		<br />
		<h2>Diógenes Rodrigues</h2>
		<Link
			hoverUnderline="right"
			href="https://github.com/dxdns"
			target="_blank"
		>
			<small>@dxdns</small>
		</Link>
	</Card>
</div>

<style>
	.gradient-border {
		--angle: 0deg;
		--primary: #39ff14;
		--secondary: #00ffff;
		border: 4px solid transparent;
		background: conic-gradient(
			from var(--angle),
			var(--secondary) 80%,
			var(--primary) 88%,
			var(--primary) 92%,
			var(--secondary) 100%
		);
		background-origin: border-box;
		background-clip: border-box;
		box-sizing: border-box;
	}
</style>
