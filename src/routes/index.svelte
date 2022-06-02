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

<main>
	<!-- <div style="left:{left}px; top:{top}px;" /> -->
    <img style="left:{left}px; top:{top}px;" src="/favicon.jpg" alt="logo"/>
</main>

<svelte:window on:keydown|preventDefault={typeKey} />

<style>
	main {
		width: 500px;
		height: 500px;
		border: solid white 2px;
		margin: 10px auto;
		position: relative;
		border-radius: 25px;
	}
	div {
		width: 50px;
		height: 50px;
		background-color: red;
		position: absolute;
		border-radius: 25px;
	}
    img {
		width: 50px;
		height: 50px;
		background-color: red;
		position: absolute;
		border-radius: 25px;
	}
</style>
