<script>
	let top = 50;
	let left = 50;
	// up = 38
	// down = 40
	// right = 39
	// left = 37
	function onKeyDown(e) {
		 switch(e.keyCode) {
			 case 38:
				 top -= 50;
				 break;
			 case 40:
				 top += 50;
				 break;
			 case 37:
				 left -= 50;
				 break;
			 case 39:
				 left += 50;
				 break;
		 }
	}
	
</script>
<style>
	main {
		width: 500px;
		height: 500px;
		border: solid blue 1px;
		margin: 10px auto;
		position: relative
	}
	div {
		width: 50px;
		height: 50px;
		background-color: green;
		position: absolute;
	}
</style>


<main>
	<div style="left: {left}px; top: {top}px">
	</div>
</main>

<svelte:window on:keydown|preventDefault={onKeyDown} />