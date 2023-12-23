<template>
    <div>
        <h2>
            {{ foodName }}
            <img src="/img_quality.svg" v-show="foodIsFavorite">
        </h2>
        <p>{{ foodDesc }}</p>
        <button @click.stop="toggleFavorite">Favorite</button>
    </div>
</template>
<script>
    export default {
        props: {
            foodName: {
                type: String,
                required: true,
                default: false,
            },
            foodDesc: {
                type: String,
                required: true,
                default: 'Apples are type of fruits that grow on trees',
            },
            isFavorite: {
                type: Boolean,
                required: true,
                default: false
            },
        },
        emits: ['toggle-favorite'],
        methods: {
            toggleFavorite() {
                this.$emit('toggle-favorite', this.foodName)
            }
        }
    }
</script>
<style scoped>
    img {
        height: 1.5rem;
        float: right;
    }
</style>