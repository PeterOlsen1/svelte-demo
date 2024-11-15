<script>
    let { todo, children } = $props();
</script>

<style>
    .grid-container {
        width: 60%;
        padding: 1em;
        border: 1px solid black;
        border-radius: 0.5em;
        display: grid;
        grid-template-columns: 1fr 4fr;
    }
    
    a, a:visited {
        color: black;
        width: 100%;
    }
</style>


<div class="grid-container">
    <div>
        <input type="checkbox">
    </div>
    <div>
        <a href="/todo/{todo.id}">
            {todo.text}
        </a>
    </div>
</div>
