<template>
  <h1>Food</h1>
  <div id="wrapper">
    <footitem 
    footName="Apple"
    Desc="Apple is a type of fruit that grow on tree."
    v-bind:isFavorite="false"/>
    <footitem
    footName="Pizza"
    Desc="Pizza has a bread base with tomato sauce, cheese, and toppings on top."
    v-bind:isFavorite="false"/>
    <footitem
    footName="Rice"
    Desc="Rice is a type of grain that people like to eat."
    v-bind:isFavorite="false"/>
    <footitem
    footName="Soup"
    Desc="I like to eat soup so much."
    v-bind:isFavorite="true"/>
    <footitem
    footName="Ice Late Coffee"
    Desc="I want to drink it all a single day."
    v-bind:isFavorite="true"/>
  </div>
</template>

<script> 
  import footitem from './components/FoodItem.vue';
  export default {
    components: {
      footitem,
    }
  }
</script>

<style scoped> 
  #wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    border: 1px dashed #000;
    background-color: lightgreen;
    padding: 10px;
    margin: 10px;
  }
</style>