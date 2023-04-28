<script>
  const infos = [
    {
      title: "Nombre",
      info: "Gabriel Pérez Licerán",
    },
    {
      title: "Profesión",
      info: "Front-End Developer",
    },
    {
      title: "Experiencia",
      info: "5 Años",
    },
    {
      title: "Email",
      info: "gapedev@gmail.com",
    },
    {
      title: "Teléfono",
      info: "601 06 87 78",
    },
    {
      title: "Github",
      info: "https://github.com/gapedev",
    },
  ];
</script>

<div class="about">
  {#each infos as info (info)}
    <div class="about__container">
      <slot name="title" title={info.title} />
      <slot name="info" info={info.info} />
    </div>
  {/each}
</div>

<style lang="scss">
  .about {
    display: grid;
    grid-template-columns: 1fr 1fr;
    border-radius: 5px;
    padding: 20px;
    margin: 20px 0;
    width: 900px;

    &__container {
      display: flex;
      align-items: center;
      padding: 10px;
    }
  }
</style>
