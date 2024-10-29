<script lang="ts">
    function makeRectangle() {
        let width = $state(100);
        let height = $state(50);

        return {
            // These need to exist within closures
            get width() {return width},
            get height() {return height},
            updateWidth: (w: number) => (width += w),
            updateHeight: (h: number) => (height += h)
        }
    }

    let rectangle = makeRectangle();
</script>

<style>
    .flex-center {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
    }
</style>

<div class="flex-center">
    <div>
        <button on:click={() => rectangle.updateWidth(10)}>
            Update width
        </button>
        <button on:click={() => rectangle.updateHeight(5)}>
            Update Height
        </button>
    </div>
    <br><br>
    <div style="width: {rectangle.width}px; height: {rectangle.height}px; background-color: black">
        
    </div>
</div>