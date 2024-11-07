<script>
	let { value = $bindable() } = $props();
</script>

<input bind:value={value} />

<style>
	input {
		font-family: 'Comic Sans MS';
		color: deeppink;
        width: 10em;
        margin-right: auto;
        margin-left: auto;
	}
</style>