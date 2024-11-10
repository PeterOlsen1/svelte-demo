<svelte:head>
    <title>Snippets</title>
</svelte:head>

<script>
    import ContentBox from './ContentBox.svelte';
    let input = $state("");
</script>

<style>
    .snippet-container {
        border: 1px solid black;
        border-radius: 8px;
        padding: 30px;
        margin-right: auto;
        margin-left: auto;
    }
</style>

{#snippet name(name)}
<div class="snippet-container">
    Hello, {name}! The user says: {input}
</div>
{/snippet}

<div class="text-container">
    <h1>
        Snippets
    </h1>
    <p>
        Snippets are an easy way we can easily remove duplicate code,
        while also parameterizing it at the same time!
        <br><br>
        Snippets can reference variables defined outside of themselves, and also reference themselves
        (given that recursion is handled properly)
        <br><br>
        For example, my snippet below only uses one variable, name, but
        it references a relative variables (that you can change) bound to
        this <input type="text" bind:value={input} placeholder="Enter some text here"> input box.
        <br>
        If I have some code as follows:
    </p>
    <div class="snippet-container">
        Hello, (name)! The user says: {input}
    </div>
    <p>
        I can turn it into a Svelte snippet, with the following syntax:
    </p>
    <div style="text-align: left">
        <code>
            &#123;#snippet name(name)&#125;<br>
            &nbsp;&nbsp;&nbsp;&nbsp;Put some html code here, using the &#123;name&#125; variable. <br>
            &nbsp;&#123;/snippet&#125;
        </code>
    </div>
    <p>
        Now, I can reuse it whenever I want with the syntax &#123;@render name(your name here)&#125;. Watch me go 😎
    </p>
    <div class="col-flex-center">
        {@render name("Peter")}
        {@render name("Jiaying")}
        {@render name("Seby")}
        {@render name("Derrick")}
    </div>    

    <p>
        Snippets are also the method of choice in Svelte 5 for passing content into components.
        Say I have some arbitrary component, 'ContentBox' where I want to pass in some HTML.
        <br>
        The inner HTML of the snippet can easily be accessed by rendering the 'children' prop.
    </p>
    <ContentBox>
        <p>
            This is me passing values into this ContentBox
        </p>
    </ContentBox>
</div>