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
        background: linear-gradient(1deg, rgba(41,46,118,1) 0%, rgba(78,82,145,1) 100%);
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