<script>
  import CajaInfo from "$lib/caja-info.svelte";
</script>

<CajaInfo>
  <h3 slot="gabi" let:nombre let:email>
    {nombre}
    {email}
  </h3>
</CajaInfo>
