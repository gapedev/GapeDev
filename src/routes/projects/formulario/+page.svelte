<script>
  import Input from "$lib/input.svelte";
  import Dropdown from "$lib/dropdown.svelte";
  import Rangos from "$lib/rangos.svelte";

  let estado = {
    nombre: "Gabi",
    apellido: "Pérez",
    sector: "FrontEnd",
    salario: {
      min: 25000,
      max: 45000,
    },
  };

  let error = null;

  let sectores = ["BackEnd", "FrontEnd", "UX Designer", "Devops", "QA"];

  function envio(e) {
    e.preventDefault();
    alert(JSON.stringify(estado));
  }

  function actualizarSalario(e) {
    estado.salario.min = e.detail.min;
    estado.salario.max = e.detail.max;

    if (estado.salario.min > estado.salario.max) {
      error = "No puedes tener más en el mínimo que en el máximo";
    } else {
      error = null;
    }
  }
</script>

<form on:submit={envio}>
  <Input identifier="nombre" label="Nombre" bind:value={estado.nombre} />
  <Input identifier="apellido" label="Apellido" bind:value={estado.apellido} />
  <Dropdown
    indentifier="sector"
    label="Sector"
    choices={sectores}
    bind:value={estado.sector}
  />
  <Rangos
    identifier="salarios"
    label="Salarios"
    min={estado.salario.min}
    max={estado.salario.max}
    on:update={actualizarSalario}
  />

  {#if error != null}
    <p>{error}</p>
  {/if}
  <p>
    <input type="submit" value="Enviar" disabled={error !== null} />
  </p>
</form>
