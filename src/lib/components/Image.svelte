<script lang="ts">
	export let src: string = '';
	export let alt: string = '';
</script>

<picture>
	<img {src} {alt} />
</picture>
