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
