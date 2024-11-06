<svelte:head>
    <title>Routing</title>
</svelte:head>

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
        Just have a +page.svelte file in (project)/routes/x/y, and any request to the url xyz.com/x/y will return the file.
    </p>

    <p>
        If you want a dynamic route, say /routing/1, for something of id 1, and /routing/2 for something of id 2,
        we can define some route folder with the syntax [name], and place a +page.svelte inside of it.

        <br><br>
        For example, a request to <a href="/routing/1">/routing/1</a> and <a href="/routing/2">/routing/2</a> will send you
        to the same page, but they display different things based on the dynamic portion of the url.
    </p>

    <p>
        These may sound a little confusing, so check out our /routes folder on the 
        <a href="https://github.com/PeterOlsen1/svelte-demo/tree/main/example/src/routes">Github</a> to
        see it in action.
    </p>
</div>