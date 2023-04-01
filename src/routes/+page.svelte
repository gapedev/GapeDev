<script>
  import Title from "$lib/title.svelte";
  import CajaInfo from "$lib/caja-info.svelte";
  import Gabi from "../../static/img/foto-gabi.jpg";
</script>

<div class="info-container">
  <div class="info-container__img">
    <img src={Gabi} alt="" />
  </div>
  <div class="info-container__info">
    <Title title="Sobre Mí" />
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus,
      asperiores!
    </p>
    <CajaInfo>
      <span slot="title" let:title>{title}:</span>
      <p slot="info" let:info>{info}</p>
    </CajaInfo>
  </div>
</div>

<style lang="scss">
  .info-container {
    display: flex;
    justify-content: space-evenly;
    padding-top: 50px;

    &__img {
      width: 400px;
    }
  }
  span {
    color: $white;
    font-weight: bold;
    padding-right: 5px;
  }

  p {
    color: $white;
  }
</style>
