<script>
  import Title from "./title.svelte";
  export let items = [];
  export let activeTabValue = 1;

  const handleClick = (tabvalue) => () => (activeTabValue = tabvalue);
</script>

<div class="container">
  <Title title="Mis Servicios" />
  <div class="section-tabs">
    <ul>
      {#each items as item}
        <li class={activeTabValue === item.value ? "active" : ""}>
          <span on:click={handleClick(item.value)}>{item.label}</span>
        </li>
      {/each}
    </ul>
    {#each items as item}
      {#if activeTabValue == item.value}
        <div class="box">
          <svelte:component this={item.component} />
        </div>
      {/if}
    {/each}
  </div>
</div>

<style lang="scss">
  .section-tabs {
    display: flex;
    flex-direction: column;
    align-items: center;

    ul {
      display: flex;

      li {
        margin: 0 10px;
      }
    }

    span {
      background-color: $white;
      padding: 5px 20px;
      border-radius: 30px;
      font-weight: bold;
      cursor: pointer;
      transition: all ease-in-out 0.3s;

      &:hover {
        color: $white;
      }
    }

    li.active > span {
      color: $white;
    }
  }
</style>
