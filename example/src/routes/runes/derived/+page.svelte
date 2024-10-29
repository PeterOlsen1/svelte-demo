<script>
	let count = $state(0);
	let doubled = $derived(count * 2);
</script>


<div>
    <h1>
        $derived Rune
    </h1>
    Here's the $derived rune. The purpose of this guy is to update whenever the variables it depends on are changed.
    <br>
    The variables must be defined with $state in order for $derived to know that it needs to change.
    <br>
    <br>

    You can also use $derived.by(callback) to do more complex calculations when some state is changed.

    <br>
    <h2>
        Example
    </h2>
    In this example, the (count) variable is a $state rune, and the doubled value is defined by $derived(count * 2)
    <br>
    <br>
    <button onclick={() => count++}>
        {doubled}
    </button>

    <p>{count} doubled is {doubled}</p>
</div>
