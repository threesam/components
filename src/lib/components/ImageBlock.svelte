<script lang="ts">
	export let caption: string = '';
	export let src: string = '';
	export let alt: string = '';

	import Image from './Image.svelte';
</script>

<figure>
	<Image {src} {alt} />
	<figcaption>{caption}</figcaption>
</figure>
