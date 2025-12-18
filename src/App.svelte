<script lang="ts">

  import Counter from './lib/Counter.svelte'
  import Header from './components/header.svelte';
  import froggyLogo from "./assets/Froggy logo.svg";
</script>
<Header />
<main>
  <div class="center content">
    <a href="https://www.thefrog.me" target="_blank" rel="noreferrer">
      <img src={froggyLogo} alt="Froggy Logo" class="logo-img" />
    </a>
  </div>
  <div class="tempdown">
    <h1>Frog's Website Wip</h1>
  </div>
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
  .tempdown{
    font: bold 1em/1.5em "FOT-Yuruka Std UB", Calibri;
  }
  .center.content{
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
  .logo-img{
    max-width: 80%;
    max-height: 80%;
    object-fit: contain;
  }

</style>