<div class="text-container">
    <h1>Svelte Routing</h1>
    <p>
        Routing in Svelte is very easy.
        <br>
        There's no 'svelte-router-dom' like we have in react.
    </p>
    <p>
        All routing in svelte is done through directory structure.
        <br>
        Routes are declared as folders within the auto generated 'routes' folder.
        <br>
        Within the folder, just define a +page.svelte file so that the compiler knows what page to return on requests.
        <br>
        <br>
        Want /x/y?
        <br>
        Just have /routes/x/y, and any request to the url xyz.com/x/y will return the file.
    </p>

    <p></p>
</div>