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
        height: 60px;
        justify-content: center;
        align-items: center;
        padding: 0 20px;
        z-index: 100;
    }
    .logo-img {
        position: absolute;
        left: 10px;
        height: 100%;
        padding: 5px;
    }
    .title {
        margin: 0;
        font-weight: bold;
        font-size: 1.5rem;
    }
</style>