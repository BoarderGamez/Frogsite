<script lang="ts">
  import radioactiveLogo from './assets/radioactive.png'
  import RoofLogo from '/roof.png'
  import Counter from './lib/Counter.svelte'
  import Header from './components/header.svelte';
</script>
<Header />
<main>
  <div>
    <a href="https://www.thefrog.me/" target="_blank" rel="noreferrer">
      <img src={RoofLogo} class="logo" alt="RUN Logo" />
      <link rel="icon" type="image/png" sizes="16x16" href={radioactiveLogo}>
    </a>
    <a href="https://www.thefrog.me" target="_blank" rel="noreferrer">
      <img src={radioactiveLogo} class="logo frog" alt="RUN Logo" />
    </a>
  </div>
  <h1>Frog's Website Wip</h1>

  <div class="card">
    <Counter />
  </div>


</main>

<style>
  main{
    padding-top: 60px;
  }
  html,body{
    margin: 0;
    padding: 0;
    height: 100%;
    overflow: auto;
  }
  .logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
  }
  .logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
  }
  .logo.frog:hover {
    filter: drop-shadow(0 0 2em #ff3e00aa);
  }

</style>
<!--no-->
