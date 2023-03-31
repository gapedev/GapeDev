<script>
  const titles = [
    "Nombre",
    "Profesión",
    "Experiencia",
    "Email",
    "Linkedin",
    "Web",
    "Teléfono",
  ];
  const info = [
    "Gabi Pérez Licerán",
    "Front-End Developer",
    "5 Años",
    "gapedev@gmail.com",
    "https://www.linkedin.com/in/gabriel-p%C3%A9rez-licer%C3%A1n-b0826a14b?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BvIfRJmdNRgCguGUgbDJ5dQ%3D%3D",
    "https://gapedev.netlify.app/",
    "601 06 87 78",
  ];
</script>

<div class="about">
  {#each titles as title}
    <span>{title}:</span>
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
