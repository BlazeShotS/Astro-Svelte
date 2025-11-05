<script lang="ts">
    import type { Snippet } from "svelte";

    let {
        children,
        text_snippet,
        texto = "",
    }: {
        children: any;
        text_snippet?:Snippet;
        texto: string;
    } = $props();
</script>

<div>
    <img src="https://inkscape.app/wp-content/uploads/imagen-vectorial.webp" alt="" style="width:400px;height:300px">
    <div>
        {#if text_snippet}
            {@render text_snippet()}
        {:else}
            <h3>{texto}</h3>
        {/if}
    </div>
    {@render children?.()}
</div>