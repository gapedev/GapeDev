<script>
  import { Motion } from "svelte-motion";
</script>

<div class="logo-home">
  <Motion
    let:motion
    whileHover={{
      scale: 1.5,
      backgroundColor: [
        "#121212",
        "rgba(131,58,180,1)",
        "rgba(253,29,29,1)",
        "rgba(131,58,180,1)",
        "#121212",
      ],
    }}
  >
    <a href="/" use:motion>GD</a>
  </Motion>
</div>

<style lang="scss">
  .logo-home {
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 2px;

    a {
      border-radius: 50%;
      width: 60px;
      height: 60px;
      color: white;
      background-color: #000;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 25px;
    }
  }
</style>
