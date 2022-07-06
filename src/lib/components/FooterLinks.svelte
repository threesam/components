<script lang="ts">
	import type { Link } from '$types';

	export let title: string = 'Title';
	export let links: Array<Link> = [];
</script>

<div class="footer-links">
	<h3>{title}</h3>
	<ul>
		{#each links as { text, href }}
			<li>
				<a {href}>{text}</a>
			</li>
		{:else}
			<li>No Links</li>
		{/each}
	</ul>
</div>

<style>
	div {
		display: flex;
		flex-direction: column;
	}

	ul {
		display: flex;
		flex-direction: column;
		gap: 0.5rem;
	}
</style>
