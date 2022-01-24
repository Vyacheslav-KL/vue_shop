<template>
    <div class="main-wrapper">
        <p>{{title}}</p>
        <catalog />
        <cart />
    </div>
</template>


<script>
    import Catalog from './catalog.vue'
    import Cart from './cart.vue'

    export default{
        name: 'main-wrapper',
        components: {
            Catalog,
            Cart
        },
        props: {},
        data() {
            return {
                title: 'Main'
            }
        }


    }
</script>


<style>
    .main {
        max-width: 900px;
        margin: 0 auto;
    }
</style>