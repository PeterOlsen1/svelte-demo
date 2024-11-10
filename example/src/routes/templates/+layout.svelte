<script>
    import MiniHeader from "$lib/components/MiniHeader.svelte";
    import MiniHeaderLink from "$lib/components/MiniHeaderLink.svelte";
</script>

<MiniHeader>
    <MiniHeaderLink ref="/templates/control-flow">Control Flow</MiniHeaderLink>
    <MiniHeaderLink ref="/templates/snippets">Snippets</MiniHeaderLink>
</MiniHeader>

<main>
    <slot />
</main>