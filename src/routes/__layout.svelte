<script lang="ts">
	import '../app.css';
	import { Nav, Footer } from '$lib';
	import type { Link } from '$types';

	// dummy content
	const links: Array<Link> = [
		{
			text: 'home',
			href: '/'
		},
		{
			text: 'about',
			href: '/about'
		}
	];
</script>

<Nav {links} />

<main>
	<slot />
</main>

<Footer />

<style>
	main {
		min-height: calc(100vh - 6rem);
	}
</style>
