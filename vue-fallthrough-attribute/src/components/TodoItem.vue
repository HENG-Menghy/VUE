<template>
    <div id="pinkBall"></div>
    <li v-bind="$attrs">{{ itemName }}</li>
    <div id="pinkBall"></div>
</template>
<script>
    export default {
        props: ['itemName']
    }
</script>
<style scoped>
    #pinkBall {
        display: inline-block;
        background-color: lightpink;
        padding: 5px;
        margin: 2px;
        border-radius: 50%;
    }
    li {
        margin: 0;
        border-radius: 10px;
        padding: 5px 10px;
    } 
</style>