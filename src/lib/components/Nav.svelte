<script lang="ts">
	import type { Link } from '$types';

	export let links: Array<Link> = [];
</script>

<header>
	<div class="corner">
		<slot name="left-corner">left</slot>
	</div>
	<nav>
		{#each links as { href, text }}
			<a {href}>{text}</a>
		{:else}
			<span>No Links</span>
		{/each}
	</nav>
	<div class="corner">
		<slot name="right-corner">right</slot>
	</div>
</header>

<style>
	header {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 0 1rem;
		box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
	}
	nav {
		height: 4rem;
		width: 100%;
		max-width: 100vw;
		display: flex;
		align-items: center;
		justify-content: center;
		gap: 1rem;
	}
	.corner {
		width: -moz-fit-content;
		width: fit-content;
	}
</style>
