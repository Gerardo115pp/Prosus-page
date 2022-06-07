<script>
    const nav_options = [
        {name:"Inicio",
        url: "#responsive-header"
        },
        {name:"Tienda",
        url: "#responsive-header"
        },
        {name:"Proyectos_Especiales",
        url: "#responsive-header"
        },
        {name:"Catalogo",
        url: "#responsive-header"
        },
       { name:"Contacto",
        url: "#responsive-header"
        }
    ]

</script>

<nav id="main-prosus-navbar" class="">
    <div class="col-span-2 justify-start items-center flex-shrink-0 text-white mr-6">
        <img src="imagenes/logo.png" width="200px" alt="logo"/>
    </div>
    <div class="block lg:hidden">
        <button id="boton" class="flex items-center px-3 py-2 border rounded text-black-200 border-black-400 hover:text-blue hover:border-black">
        <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
      </button>
    </div>
    <div id="mpn-menu" class="lg:flex lg:items-center lg:w-auto hidden">
        {#each nav_options as option}
            <a href={option.url} class="mpn-nav-option">{option.name.replace("_", " ")}</a>
        {/each}
    </div>
</nav>

<style>
    #main-prosus-navbar {
        display: flex;
        border-bottom: 1px solid #e6e6e6;
        padding: 2vh 2vw;
        justify-content: space-between;
    }

    #mpn-menu {
        display: flex;
        width: 40vw;
        justify-content: space-between;
    }

    #mpn-menu a {
        text-decoration: none;
        color: var(--theme-color);
        font-size: .7em;
    }

    #mpn-menu a:hover {
        color: #00bcd4;
    }
</style>
