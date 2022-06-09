<script>
    export let categories = [];
    export let category_clicked_handler = () => {};

</script>

<section id="prosus-store-categories">
    <div id="psc-categories-wrapper">
        {#each categories as category, index}
            <div  class="psc-cw-category-container">
                <div class="psc-cw-cc-image-wrapper">
                    <div on:click={() => category_clicked_handler(index)} class="psc-cw-cc-image">
                        <img src={category.thumbnailUrl} alt="">
                    </div>
                </div>
                <div class="psc-cw-cc-name">
                    {category.name.toLowerCase()}
                </div>
            </div>
        {/each}
    </div>
</section>

<style>
    #prosus-store-categories {
        background: var(--theme-gradient);
        padding: 5vh 0;
    }

    #psc-categories-wrapper {
        width: 80%;
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        align-items: center;
        margin: 0 auto;
    }

    .psc-cw-category-container {
        --psc-cw-image-size: 10vw;

        display: flex;
        background-clip: border-box;
        flex-direction: column;
        width: 28%;
        height: 30%;
        margin: 2vh 1.5vw;
        justify-content: center;
        align-items: center;
    }
    
    .psc-cw-cc-image-wrapper {
        display: flex;
        background: url('/imagenes/Splash.png');
        background-repeat: no-repeat;
        background-position: center;
        width: calc(var(--psc-cw-image-size) + 4vw);
        justify-content: center;
        align-items: center;
        padding: 6.4vh 0 3.4vh 0;
    }
    
    .psc-cw-cc-image {
        cursor: pointer;
        overflow: hidden;
        display: flex;
        width: var(--psc-cw-image-size);
        height: var(--psc-cw-image-size); 
        background-color: #fff;
        border-radius: 50%;
        justify-content: center;
        align-items: center;
    }

    .psc-cw-cc-name {
        margin-top: 1vh;
        font-weight: bold;
        text-transform: capitalize;
        color: white;
    }
</style>