<!-- Horse.svelte -->
<script>
	let { emote, position, reset, color, animation } = $props();
</script>

<div class="flex h-10 items-center bg-orange-900">
	<div style="width:{position}%" class="h-full shrink-0 transition-all duration-1000 {color}"></div>
	<div style="width:{reset}%" class="h-full shrink-0 transition-all duration-1000 {color}"></div>
	<div class="animal {animation}">{emote}</div>
</div>

<style>
	.animal {
		font-size: 55px;
	}

	.bounce {
		animation: bounce 0.5s infinite;
	}

	.spin {
		animation: spin 1s linear infinite;
	}
</style>
