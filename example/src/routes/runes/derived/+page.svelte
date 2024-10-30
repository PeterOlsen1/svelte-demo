<script>
	let count = $state(0);
	let doubled = $derived(count * 2);
</script>

<style> 
    button {
        width: 10em;
        margin-right: auto;
        margin-left: auto;
    }
</style>

<div class="text-container">
    <h1>
        $derived Rune
    </h1>
    <p>
        Here's the $derived rune. The purpose of this guy is to update whenever the variables it depends on are changed. <br>
        The variables must be defined with $state in order for $derived to know that it needs to change.
    </p>
    <p>
        You can also use $derived.by(callback) to do more complex calculations when some state is changed.
    </p>
    <h2>
        Example
    </h2>
    <p>
        In this example, the (count) variable is a $state rune, and the doubled value is defined by $derived(count * 2)
        <br>
        'Count' is updated any time you click the button, and therefore the 'doubled' value is updated as well.
    </p>
    <br>
    <button onclick={() => count++}>
        {doubled}
    </button>

    <p>{count} doubled is {doubled}</p>
</div>
