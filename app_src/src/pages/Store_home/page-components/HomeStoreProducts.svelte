<script>
    import ProductCard from "../../../components/ProductsCard.svelte"
    export let products = [];
</script>

<div id="home-products-content">
    <div id="hpc-products-wrapper">
        {#each products as product}
             <ProductCard product_name={product.name} product_image={product.thumbnailUrl}/>
        {/each}
    </div>
</div>

<style>
    #home-products-content {
        background: rgb(41,46,118);
        background: var(--theme-gradient);
        padding: 10vh 0;
    }

    #hpc-products-wrapper {
        width: 100%;
        display: flex;
        justify-content: space-around;
        align-items: center;
        flex-wrap: wrap;
    }
</style>