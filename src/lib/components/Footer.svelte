<script lang="ts">
	import FooterLinks from './FooterLinks.svelte';
	import type { Link } from '$types';

	const links: Array<Link> = [
		{
			text: 'Link 1',
			href: '/'
		},
		{
			text: 'Link 2',
			href: '/'
		}
	];
</script>

<footer>
	<FooterLinks title="Follow Us" {links} />
</footer>

<style>
	footer {
		/* color: var(--footerTextColor);
		background: var(--footerBackground); */
		text-align: center;
	}
</style>
