<script>
  import Gabi from "../../static/img/foto-gabi.jpg";
  import Navbar from "./navbar.svelte";
</script>

<section class="section-hero">
  <Navbar />
  <div class="section-hero__container">
    <div class="section-hero__image">
      <img src={Gabi} alt="" />
    </div>
    <div class="section-hero__info">
      <h1>Gabi Pérez</h1>
      <p>Front-End Developer</p>
    </div>
  </div>
</section>

<style lang="scss">
  .section-hero {
    background-image: $bg-gradient, url(/img/fondo.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 100%;
    position: relative;

    &__container {
      margin-top: 100px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    &__image {
      img {
        width: 240px;
        height: 240px;
        border-radius: 50%;
      }
    }

    &__info {
      text-align: center;

      h1 {
        font-size: 3rem;
        color: $secondary;
      }

      p {
        color: $white;
      }
    }
  }
</style>
