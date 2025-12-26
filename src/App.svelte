<script lang="ts">
  import { onMount } from 'svelte';
  import Header from './components/header.svelte';
  import froggyLogo from "./assets/Froggy logo.svg";
  import { Catppuccin } from './color.js';

  let scrolled = false;

  onMount(() => {
    const handleScroll = () => {
      scrolled = window.scrollY > 50;
    };
    window.addEventListener('scroll', handleScroll);
    return () => window.removeEventListener('scroll', handleScroll);
  });
</script>
<div class="page-wrapper">
  <Header />
  <main style="background-color: {Catppuccin.Base}; color: {Catppuccin.Text};">
    <div class="center content">
      <div class="hero-container" class:scrolled>
        <a href="https://www.thefrog.me" target="_blank" rel="noreferrer">
          <img src={froggyLogo} alt="Froggy Logo" class="logo-img" />
        </a>
        <h1 class="hero-title" style="color: {Catppuccin.Text};">Frogginton Frogged II COMMIT</h1>
      </div>
    </div>

    <section class="about-section">
      <h2 style="color: {Catppuccin.Text};">About Me</h2>
      <a href="https://github.com/BoarderGamez" target="_blank" rel="noreferrer" style="color: {Catppuccin.Blue};">
        Github
      </a>
    </section>
  </main>

  <footer style="background-color: {Catppuccin.Mantle}; color: {Catppuccin.Subtext0}; border-top: 1px solid {Catppuccin.Surface0};">
    <p>&copy; 2025 Frogginton Frogged II</p>
    <a href="https://github.com/BoarderGamez" target="_blank" rel="noreferrer" style="color: {Catppuccin.Blue};">GitHub</a>
  </footer>
</div>

<style>
  :global(html) {
    margin: 0;
    padding: 0;
    height: 100%;
    background-color: #eff1f5;
  }
  :global(body) {
    margin: 0;
    padding: 0;
    min-height: 100%;
    overflow-y: scroll;
    background-color: #eff1f5;
  }
  .page-wrapper {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    width: 100%;
    box-sizing: border-box;
  }
  :global(a) {
    color: #1e66f5;
  }
  :global(a:hover) {
    color: #04a5e5;
  }
  :global(a:visited) {
    color: #7287fd;
  }
  :global(::selection) {
    background-color: #7C7F933F;
  }
  main {
    padding-top: 60px;
    flex: 1;
  }
  .center.content {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
  .hero-container {
    display: flex;
    align-items: center;
    position: relative;
    width: 100%;
    justify-content: center;
  }
  .logo-img {
    max-width: 80%;
    max-height: 80%;
    object-fit: contain;
    transition: transform 0.6s ease, filter 0.3s ease;
    z-index: 2;
    position: relative;
    transform: translateX(5vw);
  }
  .logo-img:hover {
    filter: drop-shadow(0 0 1em #1e66f5);
    transform: translateX(5vw) scale(1.05);
  }
  .scrolled .logo-img:hover {
    transform: translateX(-15vw) scale(1.05);
  }
  .hero-title {
    font: bold 1em/1.5em "FOT-Yuruka Std UB", Calibri;
    font-size: 3em;
    position: absolute;
    right: 30%;
    opacity: 0;
    transform: translateX(80px);
    transition: transform 0.6s ease, opacity 0.6s ease;
    white-space: nowrap;
  }
  .scrolled .logo-img {
    transform: translateX(-15vw);
  }
  .scrolled .hero-title {
    opacity: 1;
    transform: translateX(0);
  }
  .about-section {
    text-align: center;
    padding: 2em;
  }
  .about-section h2 {
    font: bold 2em/1.5em "FOT-Yuruka Std UB", Calibri;
    margin-bottom: 1em;
  }
  .about-section a {
    font-size: 1.2em;
    text-decoration: none;
  }
  .about-section a:hover {
    text-decoration: underline;
  }
  footer {
    text-align: center;
    padding: 2em 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 0.5em;
    width: 100%;
    box-sizing: border-box;
    margin-top: auto;
    margin-left: 0;
    margin-right: 0;
  }
  footer p {
    margin: 0;
  }
  footer a {
    text-decoration: none;
  }
  footer a:hover {
    text-decoration: underline;
  }

  @media (max-width: 768px) {
    .hero-title {
      font-size: 1.5em;
      right: 5%;
    }
    .scrolled .logo-img {
      transform: translateX(-30vw);
    }
    .about-section h2 {
      font-size: 1.5em;
    }
    .about-section a {
      font-size: 1em;
    }
  }

  @media (max-width: 480px) {
    .hero-container {
      flex-direction: column;
    }
    .hero-title {
      position: relative;
      right: auto;
      font-size: 1.2em;
      opacity: 1;
      transform: none;
      margin-top: 1em;
    }
    .scrolled .logo-img {
      transform: none;
    }
    .scrolled .hero-title {
      transform: none;
    }
    .logo-img {
      max-width: 60%;
      max-height: 60%;
      transform: none;
    }
    .logo-img:hover {
      transform: scale(1.05);
    }
    .center.content {
      height: auto;
      min-height: 80vh;
      padding: 2em;
    }
    .about-section {
      padding: 1em;
    }
  }
</style>
