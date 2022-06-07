<script>
    export let categories = [];


</script>

<section id="prosus-store-categories">
    <div id="psc-categories-wrapper">
        {#each categories as category}
            <div class="psc-cw-category-container">
                <div class="psc-cw-cc-image">
                    <img src={category.thumbnailUrl} alt="">
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
        background-color: #F0F0F0;
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
        display: flex;
        flex-direction: column;
        width: 28%;
        height: 30%;
        margin: 2vh 1.5vw;
        justify-content: center;
        align-items: center;
    }
    
    .psc-cw-cc-image {
        --psc-cw-image-size: 16vw;
        
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
        color: #2F1160;
    }
</style>