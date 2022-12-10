<script lang="ts">
  import logo from './assets/svelte.png'
  import Header from './lib/Header.svelte'
  import Sidebar from './lib/Sidebar.svelte'
</script>

<main>
  <header>
    <Header />
  </header>
  <aside><Sidebar /></aside>
  <section>MAIN</section>
  <footer>FOOTER</footer>
</main>

<style>
  :root {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
      Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
    background: url('assets/table-bg.jpg');
    background-size: cover;
    background-position: center;
  }

  main {
    display: grid;
    max-width: 1200px;
    margin: 2rem auto;
    grid-template-areas:
      'header  header'
      'sidebar main  '
      'footer  footer';
    grid-template-columns: minmax(250px, 20%) 1fr;
    background-image: url('assets/ivory-paper.jpg');
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px,
      rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px,
      rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
  }
  @media (max-width: 768px) {
    main {
      grid-template-areas:
        'header   header'
        'sidebar  sidebar'
        'main     main'
        'footer  footer';
      grid-template-columns: repeat(2, 1fr);
    }
  }

  header {
    grid-area: header;
    background-color: rgba(0, 55, 128, 0.25);
  }

  aside {
    grid-area: sidebar;
  }

  section {
    grid-area: main;
    background-color: green;
  }

  footer {
    grid-area: footer;
    background-color: red;
  }
</style>
