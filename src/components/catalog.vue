<template>
    <div class="catalog">
        <h1>Catalog</h1>
        <div class="catalog__list">
        <catalog-item
            v-for="product in products"
            :key="product.name"
            v-bind:product_data="product"
            @sendData="showName"
        />
        </div>
    </div>
</template>

<script>
import CatalogItem from './catalog-item.vue'

export default {
    name: "catalog",
    components: {
        CatalogItem
    },
    props: {},
    data() {
        return {
            products: [
                {
                    image: "1.jpg",
                    name: "Samsung",
                    price: 1000,
                    article: "Discription",
                    availble: true
                },
                {
                    image: "2.jpg",
                    name: "Sony",
                    price: 1200,
                    article: "Discription",
                    availble: true
                },
                {
                    image: "3.jpg",
                    name: "Panasonic",
                    price: 8000,
                    article: "Discription",
                    availble: true
                },
                {
                    image: "4.jpg",
                    name: "Apple",
                    price: 1400,
                    article: "Discription",
                    availble: true
                }
            ]
        }
    },
    methods: {
        showName(data) {
            console.log(data)
        }
    }
}
</script>

<style lang="scss">
    .catalog {
        &__list {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
        }
    }
</style>