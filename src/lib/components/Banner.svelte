<script lang="ts">
	export let title: string = '';
	export let description: string = '';
	export let src: string = '';
	export let alt: string = '';
	export let badgeText: string = '';

	import Image from './Image.svelte';
	import Badge from './Badge.svelte';
</script>

<section>
	<!-- BADGING -->
	<Badge {badgeText} />
	<!-- IMAGE -->
	{#if src && alt}
		<figure>
			<Image {src} {alt} />
		</figure>
	{:else}
		<figure class="fallback" />
	{/if}
	<!-- CONTENT -->
	<div class="banner-content">
		{#if title}
			<h1>{title}</h1>
		{/if}

		{#if description}
			<p>{description}</p>
		{/if}
	</div>
</section>
