<script>
  import Download from "./icons/download.svelte";
  export let boton;
  export let link;
  export const download = null;
</script>

<div data-tooltip="Size: 83KB" class="button">
  <a href={link} download>
    <div class="button__wrapper">
      <div class="button__text">{boton}</div>
      <span class="button__icon">
        <Download width="30" height="30" stroke="#fff" fill="#fff" />
      </span>
    </div>
  </a>
</div>

<style lang="scss">
  .button {
    width: $width;
    height: $height;
    background: $secondary;
    position: relative;
    text-align: center;
    border-radius: 0.45em;

    &:before {
      position: absolute;
      content: attr(data-tooltip);
      width: $tooltip-width;
      height: $tooltip-height;
      background-color: $tooltip-color;
      font-size: 0.9rem;
      color: #111;
      border-radius: 0.25em;
      line-height: $tooltip-height;
      bottom: calc($height + $gap-between-tooltip-to-button + 10px);
      left: calc(50% - $tooltip-width / 2);
      opacity: 0;
      visibility: hidden;
      -webkit-transition: all 0.5s;
      transition: all 0.5s;
    }

    &:after {
      position: absolute;
      content: "";
      width: 0;
      height: 0;
      border: 10px solid transparent;
      border-top-color: $tooltip-color;
      left: calc(50% - 10px);
      bottom: calc(100% + $gap-between-tooltip-to-button - 10px);
      opacity: 0;
      visibility: hidden;
      -webkit-transition: all 0.5s;
      transition: all 0.5s;
    }

    &:hover {
      &:before {
        bottom: calc($height + $gap-between-tooltip-to-button);
        opacity: 1;
        visibility: visible;
      }

      &:after {
        bottom: calc($height + $gap-between-tooltip-to-button - 20px);
        opacity: 1;
        visibility: visible;
      }
    }

    &:hover &__text {
      top: -100%;
    }

    &:hover &__icon {
      top: 0;
    }

    &__text {
      display: -webkit-box;
      display: -ms-flexbox;
      display: flex;
      -webkit-box-align: center;
      -ms-flex-align: center;
      align-items: center;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      justify-content: center;
      top: 0;
    }

    &__text,
    &__wrapper,
    &__icon {
      overflow: hidden;
      position: absolute;
      width: 100%;
      height: 100%;
      left: 0;
      color: $white;
    }

    &__text,
    &__icon {
      -webkit-transition: top 0.5s;
      transition: top 0.5s;
    }

    &__icon {
      color: $white;
      top: 100%;
      display: -webkit-box;
      display: -ms-flexbox;
      display: flex;
      -webkit-box-align: center;
      -ms-flex-align: center;
      align-items: center;
      -webkit-box-pack: center;
      -ms-flex-pack: center;
      justify-content: center;
    }
  }
</style>
