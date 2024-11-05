<script>
    import HeaderLink from "./HeaderLink.svelte";

</script>

<style>
    nav {
        border-bottom: 1px solid black;
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
    }

</style>

<nav>
    <HeaderLink ref="/">Home</HeaderLink>
    <HeaderLink ref="/routing">Routing</HeaderLink>
    <HeaderLink ref="/runes">Runes</HeaderLink>
    <HeaderLink ref="/components">Components</HeaderLink>
</nav>