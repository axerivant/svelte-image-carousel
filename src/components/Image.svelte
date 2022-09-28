<script lang="ts">
	// import { fly } from 'svelte/transition'

	export let src: string
	export let height: string

	// $: enter = isNext ? 500 : -500
	// $: leave = isNext ? -500 : 500

	// in:fly|local={{ x: 500, delay: 200 }}
	// out:fly|local={{ x: -500, duration: 200 }}
</script>

<div class="container" style="height: {height};">
	<div class="img" style="background-image: url({src});" />
</div>

<style>
	.container {
		display: flex;
		justify-content: center;
		align-items: center;
		width: 100%;
	}
	.img {
		background-size: contain;
		background-repeat: no-repeat;
		background-position: center;
		width: 100%;
		height: 100%;
	}
</style>
