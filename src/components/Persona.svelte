<script>
    let personas = ["Abel","Miguel","Carlos"]
</script>

<div>
    {#each personas as persona}
        <div>
            <h3>{persona}:</h3>
            <p>Hola me llamo: {persona}</p>
        </div>
    {/each}
</div>
