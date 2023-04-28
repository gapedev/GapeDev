<script>
  import Logo from "./logo.svelte";
  import Links from "../services/links";
  import Github from "./icons/github.svelte";
  import Linkedin from "./icons/linkedin.svelte";
  import { Motion } from "svelte-motion";
</script>

<header class="section-header">
  <nav>
    <ul>
      {#each Links as { href, title }}
        <li>
          <a {href}>{title}</a>
          <span>&nbsp</span>
        </li>
      {/each}
    </ul>
  </nav>
  <Logo />
  <nav class="section-header__icons">
    <Motion let:motion whileHover={{ y: -2 }} whileTap={{ scale: 0.9 }}>
      <span use:motion><Github width={38} /></span>
    </Motion>
    <Motion let:motion whileHover={{ y: -2 }} whileTap={{ scale: 0.9 }}>
      <span use:motion><Linkedin width={38} /></span>
    </Motion>
  </nav>
  <nav />
</header>

<style lang="scss">
  .section-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 100px;
    width: 100%;
    ul {
      display: flex;
      gap: 25px;
    }

    li {
      display: flex;
      position: relative;
    }

    a {
      color: black;

      &:after {
        content: "";
        display: inline-block;
        background-color: $primary;
        width: 0;
        height: 2px;
        position: absolute;
        left: 0;
        bottom: 0;
        transition: width ease 0.3s;
      }
      &:hover::after {
        width: 95%;
      }
    }

    &__icons {
      display: flex;
      align-items: center;
      gap: 5px;
    }
  }

  .active {
    &:after {
      content: "";
      display: inline-block;
      background-color: $primary;
      width: 0;
      height: 2px;
      position: absolute;
      left: 0;
      bottom: 0;
      transition: width ease 0.3s;
    }
    &:hover::after {
      width: 95%;
    }
  }
</style>
