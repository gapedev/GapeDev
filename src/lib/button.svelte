<script>
  import Download from "./icons/download.svelte";

  export let boton;
  export let link;
  export const download = null;
</script>

<div class="button">
  <a href={link} download>
    <div class="button__wrapper">
      <div class="button__text">{boton}</div>
      <span class="button__icon" />
    </div>
  </a>
</div>

<style lang="scss">
  .button {
    display: flex;
    align-items: center;
    padding: 21px 17px;
    font-size: 1.2rem;
    font-weight: 600;
    text-align: center;
    border: 3px solid #000;
    border-radius: 16px;

    &:hover {
      background-color: $primary;
    }

    a {
      color: $primary;

      &:hover {
        color: $white;
      }
    }
  }
</style>
