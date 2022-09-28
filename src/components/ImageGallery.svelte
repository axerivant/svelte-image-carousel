<script lang="ts">
	import Controls from './Controls.svelte'
	import Dots from './Dots.svelte'
	import Image from './Image.svelte'

	export let images: string[]
	export let height: string

	const numOfImages = images.length - 1

	let currentImageIndex = 0
	let isHovering = false

	const controllers = {
		next: () => {
			const nextIndex = currentImageIndex + 1
			if (nextIndex > numOfImages) return
			currentImageIndex = nextIndex
		},
		previous: () => {
			const previousIndex = currentImageIndex - 1
			if (previousIndex < 0) return
			currentImageIndex = previousIndex
		},
		to: () => {
			// slide to specific image
		}
	}
</script>

<div
	class="container"
	on:mouseenter={() => (isHovering = true)}
	on:mouseleave={() => (isHovering = false)}
>
	{#each [images[currentImageIndex]] as src (currentImageIndex)}
		<Image {src} {height} />
	{/each}

	{#if isHovering}
		<Controls {controllers} />
		<Dots {images} {currentImageIndex} />
	{/if}
</div>

<style>
	.container {
		position: relative;
		overflow: hidden;
		height: 100%;
		width: 100%;
	}
</style>
