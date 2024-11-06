<script>
    let count = $state(0);
    let items = [
        {class: 'csci5117', instructor: 'Daniel Kluever'},
        {class: 'csci4131', instructor: 'Dan Challou'},
        {class: 'csci4511W', instructor: 'Andy Exley'},
        {class: 'csci3081W', instructor: 'Mattia Fazzini'},
        {class: 'math4242', instructor: 'Jiaping Wang'}
    ]

    function incrementCount() {count++;}

    function after2Seconds() {
        return new Promise((resolve) => {
            setTimeout(() => {
                resolve('I was resolved!');
            }, 2000);
        });
    }

    let promise = $state(after2Seconds());
    function resetPromise() {promise = after2Seconds();}
    function errorPromise() {
        function errorAfter2() {
            return new Promise((resolve, reject) => {
                setTimeout(() => {
                    reject('Something went horribly wrong.');
                }, 2000);
            });
        }
        promise = errorAfter2();
    }
</script>

<style>
    .item-container {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        width: 100%;
        border: 1px solid black;
        border-radius: 5px;
        margin-top: 5px;
        margin-bottom: 5px;
        padding: 10px;
    }

</style>

<svelte:head>
    <title>Control Flow</title>
</svelte:head>

<div class="text-container">
    <h1>
        Control Flow
    </h1>
    <p>
        Templating syntax in Svelt isn't hard to pick up after experience with Jinja.
        <br><br>
        These concepts are more well demonstrated when viewing the source code, but there will be some examples included.
    </p>
    <h3>
        If statements
    </h3>

    {#if count % 2 == 0}
        <p>Count is even!</p>
    {:else}
        <p>Count is odd!</p>
    {/if}
    <button onclick={incrementCount}>
        Count: {count}
    </button>

    <h3>
        Await Statement
    </h3>
    {#await promise}
        <p>Currently waiting 2 seconds...</p>
    {:then value} 
        <p>Promise was resolved! It said: {value}</p>
    {:catch error}
        <p>Something went wrong! Error was: {error}</p>
    {/await}
    <button onclick={resetPromise}>
        Run promise again
    </button>
    <br>
    <button onclick={errorPromise}>
        Run promise with error
    </button>

    <h3>
        Key statements
    </h3>
    <p>
        These will destroy and recreate content when the value of the given expression changes. This
        is used to reinstantiate and reinitialize components.
        <br>
        This will also replay any transitions.
    </p>


    <h3>
        Each Statements
    </h3>
    <p>I have a list of objects defined, this just iterates over all of them.</p>
    {#each items as item}
        <div class="item-container">
            <div>
                <b>Class:</b>
            </div>
            <div>
                {item.class}
            </div>
            <div>
                <b>Instructor:</b>
            </div>
            <div>
                {item.instructor}
            </div>
        </div>
    {/each}
</div>