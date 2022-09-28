<script lang="ts">
	import Dot from './Dot.svelte'

	export let images: string[]
	export let currentImageIndex: number
</script>

<div class="container">
	<div class="dots">
		{#each images as image, i}
			<Dot index={i} {currentImageIndex} />
		{/each}
	</div>
</div>

<style>
	.container {
		display: flex;
		justify-content: center;
	}
	.dots {
		background: rgba(0, 0, 0, 0.67);
		height: 2.5rem;
		min-width: fit-content;
		position: absolute;
		display: flex;
		bottom: 1.5rem;
		gap: 0.75rem;
		align-items: center;
		padding: 1.5rem;
		border-radius: 9999px;
	}
</style>
