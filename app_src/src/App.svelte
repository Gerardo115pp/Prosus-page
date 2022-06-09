<script>
    import { routes } from "./routes";
    import Router from "svelte-spa-router";
    import Navbar from './components/Navbar/Navbar.svelte';
    import Footer from './components/Footer/Footer.svelte';
</script>

<style>
    @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700");

    :global(:root) {
        --theme-color: #11478E;
        --green-theme-color: #05DB83;
        --purple-theme-color: #2A2F77;
        --theme-gradient: linear-gradient(90deg, #292E76 0%, #616395 100%);
        --box-roundness: 20px;
    }

    :global(body) {
        font-family: "Poppins", sans-serif;
        margin: 0;
        padding: 0;
    }
</style>


<svelte:head>
    <link
        rel="stylesheet"
        href="https://fonts.sandbox.google.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0"
    />
</svelte:head>
<div id="page-content">
    <Navbar />
    <div id="content-wrap">
        <Router {routes} />
    </div>
    <Footer/>
</div>