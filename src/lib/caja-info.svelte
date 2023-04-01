<script>
  let infos = [
    {
      nombre: "Gabi Pérez Licerán",
      profesion: "Front-End Developer",
      experiencia: "5 Años",
      email: "gapedev@gmail.com",
      linkedin:
        "https://www.linkedin.com/in/gabriel-p%C3%A9rez-licer%C3%A1n-b0826a14b?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BvIfRJmdNRgCguGUgbDJ5dQ%3D%3D",
      web: "https://gapedev.netlify.app/",
      telefono: "601 06 87 78",
    },
  ];
</script>

<div class="about">
  {#each infos as info (info)}
    <slot
      name="gabi"
      nombre={info.nombre}
      profesion={info.profesion}
      experiencia={info.experiencia}
      email={info.email}
      linkedin={info.linkedin}
      web={info.web}
      telefono={info.telefono}
    />
  {/each}
</div>

<style lang="scss">
  .about {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 10px;

    span {
      color: $white;
      font-weight: bold;
    }
  }
</style>
