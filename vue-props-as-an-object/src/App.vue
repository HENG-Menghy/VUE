<template>
  <h1>Food</h1>
  <p>Food description for the rice component is not provided so the default value is used instead.</p>
  <div id="wrapper">
    <food-item 
      foodName="Apples" 
      foodDesc="Apples are a type of fruit that grow on trees."
      :isFavorite="true"/>
    <food-item 
      food-name="Pizza"
      food-desc="Pizza has a bread base with tomato sauce, cheese, and toppings on top."
      :isFavorite="false"/>
    <food-item 
      foodName="Rice"
      
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