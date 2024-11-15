<svelte:head>
    <title>Directives</title>
</svelte:head>

<script>
	import { fly } from 'svelte/transition';

	let visible = $state(false);
</script>

<div class="text-container">
    <h1>
        Directives
    </h1>
    <p>
        Directives in Svelte are denoted by (directive):(property), and can be easily applied to
        HTML tags to enhance your site.
    </p>
    <h2>
        bind:
    </h2>
    <p>
        This directive is especially important for assigning some property to a JS expression.
        <br>
        A very common use for bind is to bind the value of an input element to some reactive variable. This means that whatever the user types in said input will be easily accessible with the bound variable.
        <br>
        It's as simple as just adding a few more characters to an input field, as seen below.
        <br><br>
        &lt;input bind:value=&#123;value&#125; /&gt;
    </p>
    <h2>
        use:
    </h2>
    <p>
        The given argument (an action function) will run once the element has been mounted. Typically, this action function will use an $effect rune so they can reset state when unmounted.
    </p>
    <h2>
        transition:
    </h2>
    <p>
        This is triggered by an element entering or leaving the DOM due to a state change. Transitions are imported from the <a href="https://svelte.dev/docs/svelte/svelte-transition">svelte/transition</a> library.
        <br>
        These transitions are bidirectional, meaning they happen both on the way in and out! Check it out for yourself down below.
        <br><br>
        <button onclick={() => visible = !visible}>Toggle Visibility</button>
    </p>
    {#if visible}
        <div transition:fly={{y: -500}}>Hello!</div>
    {/if}
    <h2>
        in: + out:
    </h2>
    <p>
        These will operate the same way as transition:, but only happen in one direction. That way, if you don't want an element repeat the same transition in both ways, you don't need to!
    </p>
    <h2>
        class:
    </h2>
    <p>
        This directive allows you to easily place classes onto tags, but also allows for conditional class placement. 
    </p>
    <h2>
        style:
    </h2>
    <p>
        Same thing as the class: directive, but with style.
    </p>
</div>