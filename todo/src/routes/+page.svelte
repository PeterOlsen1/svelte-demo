<script>
    import ListItem from "$lib/components/ListItem.svelte";
    let text = $state('')
    $inspect(text)
    let id = 4;

    let todos = $state([{
        id: 1,
        text: 'Buy milk'
    }, {
        id: 2,
        text: 'Buy eggs'
    }, {
        id: 3,
        text: 'Buy bread'
    }]);
</script>

<style>
    .todo-header {
        display: grid;
        grid-template-columns: 1fr 4fr;
        width: 60%;
        margin-right: auto;
        margin-left: auto;
        font-weight: bold;
        font-size: 16pt;
        border-bottom: 1px solid black;
    }

    .todo-container {
        display: flex;
        justify-content: center;
        flex-direction: column;
        gap: 1em;
        width: 100%;
        margin-right: auto;
        margin-left: auto;
        align-items: center;
    }
</style>

<link rel="stylesheet" href="/todoList.css">
<div class="container">
    <h1>
        TODO App
    </h1>
    <p>
        A simple TODO app made with SvelteKit
    </p>

    <br><br>
    <div class="todo-header">
        <span>Completed?</span>
        <span>Item</span>
    </div>

    <br><br>
    <div class="todo-container">
        {#each todos as todo}
            <ListItem todo={todo}></ListItem>
        {/each}
    </div>

    <br><br>

    <div>
        <input type="text" bind:value={text}>
        <button onclick={() => {todos = [...todos, {id, text}]; id++}}>Add</button>
    </div>
</div>
