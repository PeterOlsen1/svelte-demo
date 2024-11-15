<script>
    let { children} = $props();
</script>

<style>
    .header {
        padding: 1em;
        width: 100%;
        display: grid;
        grid-template-columns: 4fr 2fr 4fr;
        border-bottom: 1px solid black;


        #title {
            text-align: right;
        }

        #link {
            text-align: left;
        }
    }   
</style>

<link rel="stylesheet" href="/app.css">


<div style="width: 100vw">
    <div class="header">
        <div id="title">
             <span>TODO App</span>
        </div>
        <div>

        </div>
        <div id="link">
            <span><a href="/">Home</a></span>
        </div>
    </div>
    {@render children()}
</div>