<script>
// @ts-nocheck

    let { ref } = $props();
    let text;
    let underline;

    function hover() {
        underline.style.width = '100%';
        text.style.top = '-2px';
    }

    function stopHover() {
        underline.style.width = '0%';
        text.style.top = '0px';
    }
</script>
    
    
<style>
    a {
        height: 2em;
        display: grid;
        place-items: center;
        padding-left: 1em;
        padding-right: 1em;
        text-decoration: none;
        font-size: 13pt;
        font-weight: 500;
    }

    a:hover {
        background-color: rgba(200, 200, 200, 0.2);
    }

    .link-underline {
        width: 0%;
        background-color: black;
        height: 2px;
        display: block;
    
        transition: width 0.2s ease;
    }

    .link-text {
        position: relative;
        top: 0px;
        transition: top 0.5s ease;
    }
</style>


<a href="{ref}" onmouseenter={hover} onmouseleave={stopHover}>
    <span class="link-text" bind:this={text}>
        <slot />
        <br>
        <span class="link-underline" bind:this={underline}></span>
    </span>
</a>
    