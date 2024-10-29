<script>
    import Component from "./Component.svelte";
</script>

<div class="text-container">
    <h1>
        $props Rune
    </h1>

    <p>
        This rune is essentially used to get inputs to components. <br>
        For exmaple, if I have some 'Component.svelte' file, and I want to display it, I can write the following in this file:
    </p>
    <p>
        &lt;Component input="hello!"/&gt;
    </p>
    <p>
        In my Component.svelte file, I can write the following JavaScript:
    </p>
    <code>
        //This allows me to use 'input' as a variable. <br>
        //We can include any number of arguments in the curly braces, <br>
        //depending on the number of props. <br>
        let &#123; input &#125; = $props(); <br>
    </code>
    <p>
        Which allows me to use 'input' as a variable.
    </p>
    <br>
    <br>
    <Component input="hello!"/>
</div>