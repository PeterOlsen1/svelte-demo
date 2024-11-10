<script>
	let { children } = $props();
</script>

<style>
    .container {
        background-color: rgba(100, 100, 100, 0.2);
        padding: 20px;
        border-radius: 10px;
    }
</style>

<div class="container">
    {@render children()}
</div>