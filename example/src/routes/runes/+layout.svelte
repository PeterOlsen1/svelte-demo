<script>
    import MiniHeader from "$lib/components/MiniHeader.svelte";
    import MiniHeaderLink from "$lib/components/MiniHeaderLink.svelte";

    let { children } = $props();
</script>

<MiniHeader>
    <MiniHeaderLink ref="/runes/bindable">Bindable</MiniHeaderLink>
    <MiniHeaderLink ref="/runes/derived">Derived</MiniHeaderLink>
    <MiniHeaderLink ref="/runes/effect">Effect</MiniHeaderLink>
    <MiniHeaderLink ref="/runes/inspect">Inspect</MiniHeaderLink>
    <MiniHeaderLink ref="/runes/props">Props</MiniHeaderLink>
    <MiniHeaderLink ref="/runes/state">State</MiniHeaderLink>
</MiniHeader>

<main>
    {@render children()}
</main>
