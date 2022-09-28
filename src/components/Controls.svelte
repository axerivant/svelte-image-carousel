<script lang="ts">
	import LeftIcon from '../assets/left.svg'
	import RightIcon from './/assets/right.svg'

	export let controllers: any
</script>

<div class="controls">
	<button class="btn" on:click={controllers.previous}>
		<img src={LeftIcon} alt="left" />
	</button>
	<button class="btn" on:click={controllers.next}>
		<img src={RightIcon} alt="right" />
	</button>
</div>

<style>
	.controls {
		position: absolute;
		bottom: 50%;
		display: flex;
		justify-content: space-between;
		width: 100%;
	}
	.btn {
		background-color: rgba(0, 0, 0, 0.67);
		padding: 0.5rem;
		border-radius: 0.5rem;
		height: 5rem;
	}
	img {
		@apply h-[2rem];
	}
</style>
