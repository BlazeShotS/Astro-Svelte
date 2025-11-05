<script>
    let nombre = "Abel"
    function cambiar(){
        nombre = "Maria"
    }
</script>

<p>Hola: {nombre}</p>
<button on:click={cambiar}>cambiar</button>
