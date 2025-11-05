<script>
  let nombre = "";
  let correo = "";
  let password = "";

  let errores = { nombre: "", correo: "", password: "" };

  function validar() {
    errores = { nombre: "", correo: "", password: "" };

    if (nombre.trim()=== "") {
        errores.nombre = "Ingrese un nombre correcto";
    }
    if (correo.trim()=== "") {
        errores.correo = "Ingrese un correo valido";
    }
    if (password.trim()=== "") {
        errores.password = "Ingrese un password valido";
    }
    return !errores.nombre && !errores.correo && !errores.password;
  }

  function manejarSubmit(e) {
    e.preventDefault();
    if (validar()) {
        alert("Sesion con exito")
        console.log("Iniciado con exito")
    }
  }
</script>

<form on:submit={manejarSubmit} class="contenedor">
    <label for="">Nombre:</label>
    <input type="text" bind:value={nombre} />
    {#if errores.nombre}
      <p class="error">{errores.nombre}</p>
    {/if}
    <label for="">Correo:</label>
    <input type="email" bind:value={correo} />
    {#if errores.correo}
        <p class="error">{errores.correo}</p>
    {/if}
    <label for="">Password:</label>
    <input type="password" bind:value={password} />
    {#if errores.password}
        <p class="error">{errores.password}</p>
    {/if}
  <button type="submit" class="boton">Enviar</button>
</form>
<br>
<br>


<style>

.contenedor{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-bottom: 2rem;
}
label{
    margin: 8px 10px;
}
input{
    padding: 5px;
    border-radius: 15px;
    border: 1px solid black;
}
.error{
    color: red;
}
.boton{
    margin-top: 15px;
    background: black;
    color: white;
    padding: 8px 65px;
}

</style>