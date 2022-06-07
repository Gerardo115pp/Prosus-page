<script>
    export let product_name = "Generic Name";
    export let product_image = "https://via.placeholder.com/150";
    // export let product_price = "$0.00";
    export let product_features = [
        "Lorem Ipsum",
        "Lorem Ipsum",
        "Lorem Ipsum"
    ];
</script>

<div class="product-card-container">
    <div class="pcc-conter-wrapper">
        <div class="pcc-cw-image-wrapper">
            <img src={product_image} alt="">
        </div>
        <div class="pcc-cw-product-info">
            <h3 class="pcc-cw-info-name">
                {product_name}
            </h3>
            <ul class="pcc-cw-info-features-container">
                {#each product_features as feature}
                    <li class="pcc-cw-if-feature">{feature}</li>
                {/each}
            </ul>  
            <div class="pcc-cw-info-controls">
                <div class="pcc-cw-ic-control control-green">
                    Carrito
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    .product-card-container {
        display: flex;
        width: 30vw;
        flex-direction: column;
        border-radius: var(--box-roundness);
        background: white;
        height: 66vh;
        align-items: center;
        padding: 3vh 0;
        margin: 2vh 0;
    }

    .pcc-conter-wrapper {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100%;
        height: 100%;
    }

    .pcc-cw-image-wrapper {
        width: 80%;
        box-shadow: -2px 4px 10px 2px rgb(0 0 0 / 20%);
        border-radius: var(--box-roundness);
    }
    
    .pcc-cw-image-wrapper img {
        border-radius: var(--box-roundness);
        width: 100%;
        height: 20vh;
        object-fit: cover;
    }

    .pcc-cw-product-info {
        display: flex;
        width: 80%;
        flex-direction: column;
        margin-top: 4vh;
        height: 35vh;
        justify-content: space-between;
    }

    .pcc-cw-info-name {
        font-size: 2.5vh;
        font-weight: bold;
        color: var(--purple-theme-color);
    }

    .pcc-cw-info-features-container {
        padding: 0 0 0 2vw;
        font-size: 1em;
        font-weight: 500;
    }

    .pcc-cw-info-features-container li {
        list-style: disc;
        margin-bottom: 1vh;
    }

    .control-green {
        background: var(--green-theme-color);
        width: max-content;
        color: white;
        border-radius: calc(var(--box-roundness) - 10px);
        padding: 0.5vh 1vw;
        font-size: .8em;
        font-weight: bold;
        cursor: pointer;
    }


    @media only screen and (max-width: 768px) {
        .product-card-container {
            width: 90%;
            height: auto;
            margin: 2vh 0;
        }
    }
</style>