<script>
	import Input from './Input.svelte';

	let message = $state('hello');
</script>

<svelte:head>
    <title>Bindable</title>
</svelte:head>

<div class="text-container">
    <h1>
        $bindable Rune
    </h1>
    <p>
        This rune is special for passing data up from components to the parent application.
    </p>
    <p>
        In this case, the input field is a component, and it uses the $bindable rune to show the outward transfer of data.
        <br>
        The text where the input content is mirrored is not a part of the component.
        <br>
    </p>
    <Input bind:value={message} />
    <p>{message}</p>
</div>