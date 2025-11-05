<script>
    let personas = ["Abel","Miguel","Carlos"]
</script>

{#snippet tarjeta(nombre)}
    <div>
        <h3>{nombre}:</h3>
        <p>Hola mi nombre es: {nombre}</p>
    </div>
{/snippet}

<div>
    {#each personas as persona}
        {@render tarjeta(persona)}
    {/each}
</div>