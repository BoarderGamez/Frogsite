<script>
    import froggyLogo from '../assets/Froggy logo.svg';
    import { Catppuccin } from '../color.js';
</script>

<header class="site-header" style="background-color: {Catppuccin.Mantle};">
    <img src={froggyLogo} alt="Froggy Logo" class="logo-img" />
    <p class="title" style="color: {Catppuccin.Green};">Froggy :3</p>
</header>
<style>
    .site-header{
        display: flex;
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 5vh;
        justify-content: center;
        align-items: center;
        padding-top: 2vh;
        padding-right: 2vh;
        padding-left: 2vh;
        padding-bottom: 2vh;
        z-index: 100;
    }
    .logo-img {
        position: absolute;
        left: 10px;
        height: 100%;
        padding-top: 2vh;
        padding-right: 2vh;
        padding-left:2vh;
        padding-bottom: 2vh;
    }
    .title {
        font: bold 1em/1.5em "FOT-Yuruka Std UB", Calibri;
        margin: 0;
        font-size: 3em;
    }
</style>