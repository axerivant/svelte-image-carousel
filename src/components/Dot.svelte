<script lang="ts">
	export let index: number
	export let currentImageIndex: number

	$: isCurrentImage = index === currentImageIndex
</script>

<div
	class="dot"
	style="background-color: {isCurrentImage
		? 'rgba(255,255,255, .75)'
		: 'rgba(255,255,255, .2)'}"
/>

<style>
	.dot {
		border-radius: 0.5rem;
		height: 0.75rem;
		width: 0.75rem;
	}
</style>
