<script>
	let size = $state(50);
	let color = $state('#ff3e00');

	let canvas;

	$effect(() => {
		const context = canvas.getContext('2d');
		context.clearRect(0, 0, canvas.width, canvas.height);

		// this will re-run whenever `color` or `size` change
		context.fillStyle = color;
		context.fillRect(0, 0, size, size);
	});
</script>

<style>
    button {
        width: 10em;
        margin-right: auto;
        margin-left: auto;
        margin-top: 2px;
    }
</style>

<div class='text-container'>
    <h1>
        $effect Rune
    </h1>
    <p>
        Code contained inside of an $effect will run 'onMount' or when reactive elements are changed. <br>
        This basically means that once the page loads and the element is added to the DOM, this code runs.
    </p>
    <p>
        In this case, the canvas element is filled in after it has been 'mounted,' or added to the DOM using the $effect rune. <br>
        When the user clicks a button, the reactive 'color' variable is updated, reuslting on the $effect rune running again.
    </p>
    <br>

    <div style="width: 100px; height: 100px; margin-right: auto; margin-left: auto">
        <canvas bind:this={canvas} width="100" height="100" />
    </div>

    <button onclick={color = '#ff0000'}>
        Make Red
    </button>
    <button onclick={color = '#00ff00'}>
        Make Green
    </button>
    <button onclick={color = '#0000ff'}>
        Make Blue
    </button>
</div>