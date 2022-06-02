<script>
	var top = 50;
	var left = 50;
	// key event
	function typeKey(e) {
		if (e.keyCode === 37) {
			left -= 50;
		} else if (e.keyCode === 38) {
			top -= 50;
		} else if (e.keyCode === 39) {
			left += 50;
		} else if (e.keyCode === 40) {
			top += 50;
		}
	}
</script>

<div class="w-[500px] h-[500px] m-auto relative rounded-lg border-2 border-white">
	<img
		style="left:{left}px; top:{top}px;"
		src="/favicon.jpg"
		alt="logo"
		class="w-[50px] h-[50px] absolute rounded-full"
	/>
</div>

<svelte:window on:keydown|preventDefault={typeKey} />
