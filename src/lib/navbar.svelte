<div class="navbar">
  <a href="/"> <p><span>G</span>ape<span>D</span>ev</p></a>
  <nav>
    <ul>
      <li>
        <a href="/">Inicio</a>
      </li>
      <li>
        <a href="/projects">Proyectos</a>
      </li>
      <li>
        <a href="/projects">Currículum</a>
      </li>
      <li>
        <a href="/projects">Contacto</a>
      </li>
    </ul>
  </nav>
</div>

<style lang="scss">
  .navbar {
    display: flex;
    justify-content: space-around;
    align-items: center;
    padding-top: 30px;

    ul {
      display: flex;
    }

    li {
      padding-right: 30px;
    }

    a {
      color: $white;
      font-weight: bold;
      font-size: 1.1rem;
      transition: all ease-in-out 0.3s;

      &:hover {
        color: $secondary;
      }
    }

    p {
      font-size: 2rem;
      color: $secondary;
      font-weight: bold;
    }

    span {
      color: $white;
    }
  }
</style>
