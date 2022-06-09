<footer id="prosus-ah-oles-footer">
    <div id="prosus-ah-oles-call-to-action">
        <h3 id="prosus-ah-oles-top-call-to-action">¡Conoce más acerca de</h3>
        <h3 id="prosus-ah-oles-mid-call-to-action">nuestros productos!</h3>
        <h3 id="prosus-ah-oles-bottom-call-to-action">Descarga <a href="#responsive-header" class="footer-ah-oles-here-link">aquí</a> nuestro catálogo</h3>
    </div>
    <div id="prosus-ah-oles-hand">
        <img src="/imagenes/hand.png" alt="" srcset="">
    </div>
    <div id="footer-prosus-ah-oles-logo">
        <img src="imagenes/logo.png " alt="" />
    </div>
</footer>

<style>
    #prosus-ah-oles-footer {
        width: 100%;
        overflow-x: hidden;
        position: relative;
        height: 75vh;
    }

    #prosus-ah-oles-call-to-action {
        position: absolute;
        left: 40%;
        top: 30%;
        font-size: 2.2rem;
        color: var(--theme-color);
    }

    #prosus-ah-oles-mid-call-to-action {
        font-weight: bold;
    }

    #prosus-ah-oles-bottom-call-to-action {
        font-size: 1.8rem;
        font-weight: lighter;
    }

    .footer-ah-oles-here-link {
        color: var(--green-theme-color);
        text-decoration: underline;
    }

    #prosus-ah-oles-hand {
        position: absolute;
        left: 13%;
        top: 47%;
        transform: translate(-50%, -50%);
    }

    #prosus-ah-oles-hand img{
        width: 30vw;
    }


    #footer-prosus-ah-oles-logo {
        position: absolute;
        width: 20vw;
        left: 13%;
        top: 90%;
        transform: translate(-50%, -50%);
    }

    #footer-prosus-ah-oles-logo img {
        width: 100%;
    }

    @media only screen and (max-width: 768px) {

        #prosus-ah-oles-footer {
            height: 40vh;
        }

        #prosus-ah-oles-hand {
            left: 24%;
            top: 50%;
        }

        #prosus-ah-oles-hand img {
            width: 50vw;
        }

        #prosus-ah-oles-call-to-action {
            left: 50%;
            top: 50%;
            transform: translate(-50%, -50%);
        }

        #prosus-ah-oles-call-to-action {
            font-size: 1rem;
            width: 60%;
            left: 74%;
        }

        #prosus-ah-oles-bottom-call-to-action {
            font-size: .8rem;
            font-weight: lighter;
        }

        #footer-prosus-ah-oles-logo {
            width: 60vw;
            left: 38%;
            top: 87%;
        }
    }        
</style>