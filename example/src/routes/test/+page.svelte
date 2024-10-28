<script>
    let count = $state(0);

    function increment() {
        count += 1;
    }
</script>

<div>
    <h1>
        Hello!
    </h1>

    <br>
    <div>
        Count = {count}
    </div>
    <button on:click={increment}>
        Click me!
    </button>
</div>