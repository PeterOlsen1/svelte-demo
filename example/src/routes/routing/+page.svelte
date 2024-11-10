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

    <h2>
        Special Pages
    </h2>
    <p>
        These special pages are more on the SvelteKit side of things, since they deal with more of the metaframework aspects, and not so much the user interface aspects.
        There are a few more special pages than just +page.svelte and +layout.svelte such as:
    </p>
    <div style="text-align: left; line-height: 1.5em">
        <ul>
            <li>
                +error.svelte
                <ul>
                    <li>
                        This page allows us to create a custom page for when errors inevitably occur.
                    </li>
                </ul>
            </li>
            <li>
                +page.(js/ts)
                <ul>
                    <li>This file is typically where data is loaded and passed into the main +page.svelte.</li>
                    <li>The same also exists for +layout.(js/ts), with the same functionality.</li>
                </ul>
            </li>
            <li>
                +(layout/page).server.(js/ts)
                <ul>
                    <li>
                        Load data for some page or layout but only on the server side.
                    </li>
                    <li>
                        This differs from +page.js since these operations will run on the serverside, keeping them secret from the client.
                    </li>
                </ul>
            </li>
            <li>
                +server.(js/ts)
                <ul>
                    <li>
                        This file is used to define a server endpoint within a route.
                    </li>
                    <li>
                        If you wanted to make some sort of API with Svelte, this would be the place to do it.
                    </li>
                </ul>
            </li>
        </ul>
    </div>
</div>