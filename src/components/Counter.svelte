<script>
  let contador = 0;
</script>

<h1>Contador:{contador}</h1>

<div class="counter">
  <button on:click={() => contador++}>+1</button>
</div>


  <style>
    .counter {
      display: grid;
      place-items: center;
      margin: 1rem;
    }
    button {
      background-color: #ff3e00;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 8px;
      font-size: 1rem;
      cursor: pointer;
    }
  </style>