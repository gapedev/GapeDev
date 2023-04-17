<script>
  import Title from "$lib/title.svelte";
  import CajaInfo from "$lib/caja-info.svelte";
  import Gabi from "../../static/img/foto-gabi.jpg";
  import Button from "$lib/button.svelte";
  import curriculum from "../../static/archivos/curriculum-dev.pdf";
  import HomeTabs from "../sections/homeTabs.svelte";
</script>

<div class="info-container container">
  <div class="info-container__img">
    <img src={Gabi} alt="" />
  </div>
  <div class="info-container__info">
    <Title title="Sobre Mí" />
    <p>
      Durante los últimos 5 años he trabajado de Front-End, desarrollando
      aplicaciones web totalmente reponsive, con flex design. Ahora, estoy
      aprendiendo varios frameworks, entre ellos Svelte y React, para aumentar
      mi conocimiento y aparte de maquetar, poder crear las aplicaciones desde
      0.
    </p>
    <CajaInfo>
      <span slot="title" let:title>{title}:</span>
      <p slot="info" let:info>{info}</p>
    </CajaInfo>
    <Button link={curriculum} download="true" boton="Descargar CV" />
  </div>
</div>

<HomeTabs />

<style lang="scss">
  .info-container {
    display: grid;
    grid-template-columns: 0.6fr 1fr;

    &__img {
      width: 500px;
    }
  }
  span {
    color: $white;
    font-weight: bold;
    padding-right: 5px;
  }

  p {
    color: $white;
    line-height: 1.5;
  }
</style>
