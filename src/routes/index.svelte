<script>
	var up = 50;
	var left = 50;
	var move = 10;
	// key event
	function typeKey(e) {
		if (e.keyCode === 37 && left !== 0) {
			left -= move;
		} else if (e.keyCode === 38 && up !== 0) {
			up -= move;
		} else if (e.keyCode === 39) {
			left += move;
		} else if (e.keyCode === 40) {
			up += move;
		}
	}
</script>

<!-- get scroll x and y check if 0 and 0 -->
<div
	class="overflow-x-scroll overflow-y-scroll  w-[500px] h-[500px] m-auto relative rounded-lg border-2 border-black"
>
	<img
		style="left:{left}px; top:{up}px;"
		src="/car.jpg"
		alt="logo"
		class="w-[50px] h-[50px] absolute rounded-full"
	/>
</div>

<svelte:window on:keydown|preventDefault={typeKey} />
