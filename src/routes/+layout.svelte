<script>
  import Navbar from "$lib/navbar.svelte";
  export const prerender = true;
  export const csr = false;
</script>

<Navbar />
<main><slot /></main>
