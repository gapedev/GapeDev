<script>
  import Dev from "../../static/img/foto-dev.png";
  import Button from "$lib/button.svelte";
  import { Motion } from "svelte-motion";
  const quote = {
    initial: {
      opacity: 0,
      x: 50,
    },
    animate: {
      opacity: 1,
      x: 0,
      transition: {
        duration: 1,
        delay: 0.5,
        staggerChildren: 0.08,
      },
    },
  };
</script>

<div class="info-container container">
  <div class="info-container__img">
    <img src={Dev} alt="" />
  </div>
  <article class="info-container__info">
    <Motion let:motion variants={quote} initial="initial" animate="animate">
      <h1 use:motion>turning vision into reality with code and design</h1>
    </Motion>
    <p>
      For the last 5 years I have worked as Front-End, developing fully
      responsive web applications, with flex design. Now, I'm learning several
      frameworks, including Svelte and React, to increase my knowledge and apart
      from layout, to be able to create applications from 0.
    </p>
    <div class="info-container__buttons">
      <Button href="/archivos/curriculum-dev.pdf" download="Currículum"
        >Currículum</Button
      >
      <a href="mailto:gapedev@gmail.com" target="_blank">Contact</a>
    </div>
  </article>
</div>

<style lang="scss">
  .info-container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    text-align: center;
    overflow: hidden;

    &__img {
      img {
        width: 100%;
      }
    }
    &__info {
      h1 {
        text-transform: capitalize;
        font-weight: bold;
        display: inline-block;
        font-size: 5rem;
        text-align: left;
      }

      p {
        margin-top: 20px;
        text-align: left;
        display: inline-block;
        opacity: 0.7;
        font-size: 1.3rem;
      }
    }
    &__buttons {
      display: flex;
      align-items: center;
      margin-top: 20px;
      gap: 20px;

      a {
        color: $primary;
        font-size: 1.3rem;
        border-bottom: 2px solid $primary;
      }
    }
  }
  span {
    color: $white;
    font-weight: bold;
    padding-right: 5px;
  }

  p {
    line-height: 1.5;
  }
</style>
