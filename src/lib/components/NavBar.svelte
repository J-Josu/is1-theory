<script lang="ts">
  import SolvedLogo from '$cmps/SolvedLogo.svelte';
</script>

<header>
  <nav>
    <ul>
      <li>
        <a
          href="https://www.info.unlp.edu.ar/"
          target="_blank"
          rel="noopener noreferrer">Facultad</a
        >
      </li>
      <li>
        <a
          href="https://is1-teoria.vercel.app/"
          target="_blank"
          rel="noopener noreferrer"
          class="logo"><SolvedLogo height="1.5rem" /></a
        >
      </li>
      <li>
        <a
          href="https://asignaturas.info.unlp.edu.ar/course/view.php?id=44"
          target="_blank"
          rel="noopener noreferrer">Catedra</a
        >
      </li>
    </ul>
  </nav>
</header>

<style>
  header {
    display: flex;
    align-items: center;
    z-index: 1;
    width: 100%;
    height: 3rem;
    position: sticky;
    top: 0;
    background-color: var(--soft-beige-1);
    backdrop-filter: blur(2px);
    box-shadow: 5px 0 10px 1px hsl(0, 0%, 80%);
    transition: background-color 1s ease-out;
    color: var(--dark-green-2);
  }
  header:hover {
    background-color: var(--soft-beige-2);
  }
  nav {
    margin-inline: auto;
    width: 100%;
    max-width: 95vw;
  }
  @media screen and (min-width: 688px) {
    nav {
      max-width: 90vw;
    }
  }
  @media screen and (min-width: 992px) {
    nav {
      max-width: 80vw;
    }
  }
  @media screen and (min-width: 1312px) {
    nav {
      max-width: 70vw;
    }
  }
  ul {
    display: flex;
    align-items: center;
    width: 100%;
    justify-content: space-around;
  }
  li {
    font-size: 1.5rem;
    padding: 0.25rem;
  }
  a {
    position: relative;
    padding: 0;
    border: none;
    opacity: 0.8;
    font-weight: bolder;
  }
  a::before {
    z-index: -1;
    content: '';
    position: absolute;
    width: 0%;
    bottom: 0;
    left: 50%;
    border-bottom: 2px solid var(--dark-green-1);
    opacity: 1;
    transition: width 0.5s ease, left 0.5s ease;
  }
  a:hover {
    opacity: 1;
  }
  a:hover::before {
    width: 100%;
    left: 0px;
  }
  .logo::before {
    border-color: hsl(45, 100%, 50%);
  }
</style>
