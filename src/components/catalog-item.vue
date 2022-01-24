<template>
    <div class="catalog-item">
        <img class="catalog-item__img" :src=" require('../assets/images/' + product_data.image) " alt="img">
        <p class="catalog-item__name">{{product_data.name}}</p>
        <p class="catalog-item__price">{{product_data.price}} $</p>
        <button class="catalog-item__add-btn btn" @click="sendData">Add</button>
    </div>
</template>

<script>
export default {
    name: "catalog-item",
    props: {
        product_data: {
            type: Object,
            default() {
                return {}
            }
        }
    },
    data() {
        return {}
    },
    methods: {
        sendData() {
            this.$emit('sendData', this.product_data.name)
        }
    }
}
</script>

<style lang="scss">
    .catalog-item {
        flex-basis: 25%;
        box-shadow: 0 0 8px 0 #1d1b1b;
        padding: $padding*2;
        margin-bottom: $margin*2;
        &__img {
            width: 50px;
        }
    }
</style>