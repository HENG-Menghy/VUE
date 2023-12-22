<template>
    <div>
        <h2>
            {{ foodName }}
            <img src="/img_quality.svg" v-show="isFavorite">
        </h2>
        <p>{{ foodDesc }}</p>
        <button @click.stop="toggleFavorite">Favorite</button>
    </div>
</template>
<script>
    export default {
        props:  ['foodName', 'foodDesc', 'isFavorite'],
        emit: ['toggle-favorite'],
        methods: {
            toggleFavorite() {
                this.$emit('toggle-favorite', this.foodName)
            }
        }
    }
</script>
<style scoped>
    img {
        float: right;
        height: 1.5rem;
    }
    button {
        margin: 20px 0 15px;
    }
    p {
        text-align: justify;
        margin: 0 10px;
    }
</style>