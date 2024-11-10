<script>
    import MiniHeader from "$lib/components/MiniHeader.svelte";
    import MiniHeaderLink from "$lib/components/MiniHeaderLink.svelte";

    let { children } = $props();
</script>

<MiniHeader>
    <MiniHeaderLink ref="/templates/control-flow">Control Flow</MiniHeaderLink>
    <MiniHeaderLink ref="/templates/snippets">Snippets</MiniHeaderLink>
</MiniHeader>

<main>
    {@render children()}
</main>