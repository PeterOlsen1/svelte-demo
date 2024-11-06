<script>
    import Component from "./Component.svelte";
    
    let input = $state('hello!');
</script>

<svelte:head>
    <title>Props</title>
</svelte:head>

<div class="text-container">
    <h1>
        $props Rune
    </h1>

    <p>
        This rune is essentially used to get inputs to components. <br>
        For exmaple, if I have some 'Component.svelte' file, and I want to display it, I can write the following in this file:
    </p>
    <pre>
        <code class="language-html">
            &lt;Component input="hello!"/&gt;
        </code>
    </pre>
    <p>
        In my Component.svelte file, I can write the following JavaScript:
    </p>
    <pre>
        <code class="language-javascript">
            //This allows me to use 'input' as a variable. <br>
            //We can include any number of arguments in the curly braces, <br>
            //depending on the number of props. <br>
            let &#123; input &#125; = $props(); <br>
        </code>
    </pre>
    <p>
        In the component, I define the following within my container:
    </p>
    <pre>
        <code class="language-html">
            &lt;div class="container"&gt;
                The user input was: &#123; input &#125;
            &lt;/div&gt;
        </code>
    </pre>
    <p>
        Therefore, when I use 'input' as a variable, I can get something like this:
    </p>
    <br>
    <Component input={input}/>

    <br>
    <p>
        These props can also be reactive.
        <br>
        This means that I can define some reactive variable, bind it to the value of this input, and then pass it into my component.
        <br>
        Once this all happens, the component text reacts to the input text!
    </p>
    <input bind:value={ input }>
</div>