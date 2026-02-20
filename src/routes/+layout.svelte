<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import Meta from '$lib/layout/meta.svelte';
	import Footer from '$lib/components/Footer.svelte';
	let { children } = $props();
</script>

<svelte:head><link rel="icon" href={favicon} /><Meta /></svelte:head>
<main class="element content-grid">
	<article class="my-42 prose">
		{@render children()}
	</article>
</main>
<Footer />

<style>
	.element::after {
		transition: transform 0.2s ease-in;
		content: '';
		position: fixed;
		overflow: hidden;
		inset: 0;
		width: 55%;
		height: 100%;
		background-image: url('/techsup.jpg');
		background-repeat: repeat;
		background-position: center;
		background-size: 8vw;
		transform: translateX(0%) rotate(5deg) scale(1.2);
		opacity: 0.05;
		z-index: -1;
	}
</style>
