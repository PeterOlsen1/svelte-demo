<script>
    import HeaderLink from "./HeaderLink.svelte";

</script>

<style>
    nav {
        width: 100%;
        border-bottom: 1px solid black;
        display: flex;
        justify-content: space-evenly;
        flex-wrap: wrap;
    }

</style>

<nav>
    <slot />
</nav>