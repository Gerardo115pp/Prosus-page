<div id="home-category-desc-content">
    <div id="hcdc-content-wrapper">
        <div id="hcdc-category-desc">
            <h3 id="hcdc-category-label">Categoria</h3>
            <p id="hcdc-category-desc">
                Lorem ipsum dolor sit, amet consectetur adipisicing elit. Earum vitae dolorem reiciendis voluptate odio facere perspiciatis non praesentium esse tempore. Doloremque inventore, culpa nam aliquam temporibus velit quibusdam nihil tempore!
            </p>
        </div>
        <div id="hcdc-category-video">
            <img src="/imagenes/video-placeholder.png" alt="" srcset="">
        </div>
    </div>
</div>

<style>
    #home-category-desc-content {
        background-color: #F0F0F0;
        padding: 5vh 0;
    }

    #hcdc-content-wrapper {
        width: 80%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin: 0 auto;
    }

    #hcdc-category-desc {
        width: 65%;
        user-select: none;
    }

    #hcdc-category-desc h3 {
        font-size: 2.5vw;
        font-weight: bold;
        color: var(--theme-color);
        margin: 0;
    }

    #hcdc-category-desc p {
        font-size: .8em;
        color: var(--purple-theme-color);
        margin: 4vh 0 0 0;
    }

    #hcdc-category-video {
        border-radius: var(--boxes-roundness);
    }
    
    #hcdc-category-video img {
        width: 100%;
        height: 100%;
        border-radius: var(--box-roundness);
    }


    @media only screen and (max-width: 768px) {
        #hcdc-content-wrapper {
            flex-direction: column-reverse;
        }

        #hcdc-category-desc {
            width: 90%;
        }
        
        #hcdc-category-desc h3 {
            font-size: 6.5vw;
            margin-top: 4vh;
        }
    }
</style>