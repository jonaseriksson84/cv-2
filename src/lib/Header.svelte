<script lang="ts">
  import src from '../assets/jonas-bw-size.png'
  import hiatus from '../assets/hiatus.otf'
</script>

<div class="wrapper">
  <img {src} alt="Portrait of Jonas" />
  <div class="title">
    <span>Hello! My name is...</span>
    <h1>Jonas Eriksson</h1>
    <span>...and I am Fullstack Engineer</span>
  </div>
</div>

<style>
  @font-face {
    font-family: 'hiatus';
    src: url('../assets/hiatus.otf') format('opentype');
  }
  .wrapper {
    display: grid;
    grid-template-columns: 0.2fr 0.75fr;
    justify-items: center;
  }
  img {
    border-radius: 50%;
    margin: 1rem;
  }
  .title {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: rgba(17, 12, 12, 0.75);
  }
  h1 {
    font-family: 'hiatus', sans-serif;
    font-size: 5rem;
    margin: 0;
  }
  span {
    align-self: start;
  }
  span:last-of-type {
    align-self: end;
  }
  @media (max-width: 500px) {
    .wrapper {
      grid-template-columns: 1fr;
      padding-bottom: 2rem;
    }
    img {
      width: 40%;
    }
    h1 {
      font-size: 3.5rem;
      margin: 0 auto;
    }
    span {
      font-size: 0.8rem;
    }
  }
</style>
