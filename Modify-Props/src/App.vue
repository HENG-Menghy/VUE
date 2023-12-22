<template>
  <h1>Food</h1>
  <p>The user can now change the favorite status of the food items with the use of a new data property initialized by the 'is-favorite' prop value.</p>
  <div id="wrapper">
    <food-item 
      foodName="Apples" 
      foodDesc="Apples are a type of fruit that grow on trees."
      :isFavorite="true"/>
    <food-item 
      foodName="Pizza"
      foodDesc="Pizza has a bread base with tomato sauce, cheese, and toppings on top."
      :isFavorite="false"/>
    <food-item 
      foodName="Rice"
      foodDesc="Rice is a type of grain that people like to eat."
      :isFavorite="false"/>
  </div> 
</template>
<script>
  import FoodItem from './components/FoodItem.vue'
  export default {
    components: {
      'food-item': FoodItem
    }
  }
</script>
<style scoped>
  #wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    border: dashed black 1px;
    flex-basis: 120px;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style>