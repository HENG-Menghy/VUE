<template>
    <div>
        <h2>
            {{ foodName }}
            <img src="/img_quality.svg" v-show="isFavorite">
        </h2>
        <p>{{ foodDesc }}</p>
    </div>
</template>
<script>
    export default {
        props: {
            foodName: {
                type: String,
                required: true
            },
            foodDesc: {
                type: String,
                required: false,
                default: 'This is the default description',
                validator: function(value) {
                    if( 30<value.length && value.length<50 ) {
                        return true;
                    } else {
                        return false;
                    }
                }
            },
            isFavorite: {
                type: Boolean,
                required: false,
                default: false
            }
        }
    }
</script>
<style scoped>
    img {
        float: right;
        height: 1.5rem;
    }
</style>