<script>
    //Import component here
    
    //Declare variables here

    //add list of TODOs here
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
        <!-- Do the for each loop in here -->
    </div>

    <br><br>

    <div>
        <!-- Logic for input and adding TODO here! -->
    </div>
</div>
