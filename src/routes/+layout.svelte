<script>
  import "../../static/styles.scss";
  import Hero from "$lib/hero.svelte";
  import Title from "../lib/title.svelte";
  import CajaInfo from "../lib/caja-info.svelte";
</script>

<Hero />
<Title title="Sobre Mí" />
<CajaInfo />
<slot />
