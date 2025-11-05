<script>
    import { untrack } from "svelte";
    import Item from "../Svelte5.svelte/Item.svelte";

    let count = $state(0);
    let count2 = $derived(count * 2);
    let nombres= ['Abel','Miguel','Juan'];
    let mostrar = $state(false);
    let mensaje = $state("Se ejecuto:");

    
    $effect(() => {
    console.log("Efecto ejecutado, count:", count, "count2:", count2);
        untrack(() => {
            mensaje = `El contador vale ${count} (doble: ${count2})`;
        });
    });

</script>


<button onclick = {() => count++} >{count}</button>
<p>Doble de contador: {count2}</p>
<p style="color: blue;">{mensaje}</p>



<button onclick={()=>mostrar = !mostrar}> Mostrar nombres</button>
{#if mostrar}
    {#each nombres as nombre}
        <p>{nombre}</p>
    {/each}
{/if}

<h1>Imagenes:</h1>
<Item texto="Hola lorito">
</Item>





<style>

</style>