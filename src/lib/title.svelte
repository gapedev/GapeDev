<script>
  export let title;
</script>

<div class="title">
  <h2>{title}</h2>
</div>

<style lang="scss">
  .title {
    h2 {
      color: $white;
      font-size: 2rem;
      font-weight: bold;
      position: relative;

      &:before {
        content: "";
        background-color: $secondary;
        width: 50px;
        height: 3px;
        position: absolute;
        top: 40px;
        left: 0;
      }
    }
  }
</style>
