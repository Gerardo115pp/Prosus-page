<script>
    import HomeHeader from "./page-components/HomeHeader.svelte";
    import HomeCategoriesSection from "./page-components/HomeCategoriesSection.svelte";
    import HomeMiddleBanner from "./page-components/HomeMiddleBanner.svelte";
    import HomeCategoryDesc from "./page-components/HomeCategoryDesc.svelte";
    import HomeStoreProducts from "./page-components/HomeStoreProducts.svelte";
    import { onMount } from "svelte";

    let store_products = [];
    let store_categories = [];
    let current_category = undefined;
    $: category_items = getCurrentCategoryProducts(current_category);

    const ecwid_api_url = 'https://app.ecwid.com/api/v3/73530757';

    const headers = {
        'Accept': 'application/json',
        'Authorization': 'Bearer public_ZE7TN14Xk6R7T3zhF3m23Bs8Ws2YWXeJ'
    };
    
    let price_formatter = new Intl.NumberFormat('es-MX', {
            style: 'currency',
            currency: 'MXN',
            minimumFractionDigits: 2
        });

    onMount(() => {
        getStoreCategories()
    });


    const getStoreCategories = () => {
        fetch(`${ecwid_api_url}/categories`, { method: 'GET', headers: headers})
            .then(response => response.json())
            .then(categories_data => {
                store_categories = categories_data.items;
                getStoreItems();
            })
        }
        
        const getStoreItems = () => {
            fetch(`${ecwid_api_url}/products`, {headers: headers, method: 'GET'})
            .then(promise => promise.json())
            .then(json_data => {
                store_products = json_data.items;
                current_category = store_categories[0];
                console.log(store_products);
            });
    }

    const getCurrentCategoryProducts = category_id => {
        if (current_category === undefined) return [];

        let products = store_products.filter(product => product?.categoryIds?.includes(current_category.id));
        return products;
    }


    const handleCategoryChange = index => {
        if (index < store_categories.length) {
            current_category = store_categories[index];
        }
    }

</script>


<main id="home-store-prosus">
    <HomeHeader />
    <HomeCategoriesSection categories={store_categories}/>
    <HomeMiddleBanner/>
    <HomeCategoryDesc/>
    <HomeStoreProducts products={category_items}/>
</main>