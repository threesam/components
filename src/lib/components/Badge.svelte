<script lang="ts">
	export let badgeText: string = '';
</script>

{#if badgeText}
	<span>{badgeText}</span>
{/if}
