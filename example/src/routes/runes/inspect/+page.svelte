<script>
	let count = $state(0);
	let message = $state('hello');

	$inspect(count, message); // will console.log when `count` or `message` change
</script>

<style>
    button, input {
        width: 10em;
        margin-right: auto;
        margin-left: auto;
    }
</style>
<div class="text-container">
    <h1>
        $inspect Rune
    </h1>
    <p>
        This rune is not as useful on the DOM as others. As the name implies, it is used with 'inspect element'.
        <br>
        Any dynamic arguments to this will trigger a console.log when changed.
        <br>
        Check it out in the developer console with this button!
    </p>
    <button onclick={() => count++}>Increment</button>
    <br>
    <input bind:value={message} />
</div>