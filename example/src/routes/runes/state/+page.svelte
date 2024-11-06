<script>
    let count = $state(0);

    function increment() {
        count += 1;
    }

    import Rectangle from "./rectangle.svelte";
</script>

<svelte:head>
    <title>State</title>
</svelte:head>

<div class="text-container">
    <h1>
        $state Rune
    </h1>
    <p>
        The state rune is extremley important when it comes to using Svelte to its fullest.
        <br>
        <br>
        Any variable defined with the $state() rune will automatically update its value on the DOM
        whenever it gets changed. For example, I have defined a count variable, set to $state(0).
        Every time the 'Click me!' button is pressed, it will call a function to increment count.
        This means that every click will update count, which will be reflected on the DOM.
        <br>
        <br>
        This is a super easy way to store reactive states.
    </p>
    <div>
        Count = {count}
    </div>
    <button onclick={increment}>
        Click me!
    </button>
    <p>
        The rectangle example down here was also created using the $state rune.
    </p>

    <Rectangle></Rectangle>
</div>
