<script>
	let { value = $bindable(), ...props } = $props();
</script>

<input bind:value={value} {...props} />

<style>
	input {
		font-family: 'Comic Sans MS';
		color: deeppink;
        width: 10em;
        margin-right: auto;
        margin-left: auto;
	}
</style>