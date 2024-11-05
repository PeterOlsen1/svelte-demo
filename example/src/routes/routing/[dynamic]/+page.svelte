<script>
    import { page } from '$app/stores';
  
    let page_name = $page.params.dynamic;
</script>


<div class="text-container">
    <p>
        You requested to /routing/{page_name}
    </p>
</div>