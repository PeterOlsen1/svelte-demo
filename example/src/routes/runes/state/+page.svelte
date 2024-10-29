<script>
    let count = $state(0);

    function increment() {
        count += 1;
    }

    import Rectangle from "./rectangle.svelte";
</script>

<div>
    <h1>
        Hello!
    </h1>

    <br>
    <div>
        Count = {count}
    </div>
    <button onclick={increment}>
        Click me!
    </button>


    <div style="width: {count}px; height: {count}px; background-color: black; margin: 1.5em;"></div>

    <Rectangle></Rectangle>
</div>
