<template>
  <h1>Food</h1>
  <p>Each food item created with v-for is now identified uniquely with the key attribute, and the problem is fixed. The favorite image now stays with the 'Fish' element, and is not transferred to 'Cake'.</p>
  <button @click="removeItem">Remove Item</button>
  <div id="wrapper">
    <food-item
    v-for="item in Foods"
    :key="item.name"
    :foodName="item.name"
    :foodDesc="item.desc"
    :isFavorite="item.fav"
    @toggle-favorite="recieveEmit"/>
  </div>
</template>

<script>
  import FoodItem from './components/FoodItem.vue';
  export default {
    components: {
      'food-item': FoodItem
    },
    data() {
      return {
        Foods: [
          {name: 'Apple', desc: 'Apples are type of fruit that grow on trees.', fav: true},
          {name: 'Pizza', desc:'Pizza is a popular Italian dish consisting of a round, flattened base of dough topped with tomato sauce, cheese, and various ingredients such as meats, vegetables, and herbs.', fav: false},
          {name: 'Rice', desc: 'Rice is eaten for energy. Everybody like to eat.', fav: true},
          {name: 'Hot soup', desc: 'Hot soups are additionally characterized by boiling solid ingredients in liquids in a pot until the flavors are extracted, forming a broth.', fav: false},
        ]
      }
    },
      methods: {
        recieveEmit(myFood) {
          const foundFood = this.Foods.find(food => food.name == myFood);
          foundFood.fav = !foundFood.fav
        },
        removeItem() {
          this.Foods.splice(1,1)
        }
      } 
   }
</script>

<style scoped>
  #wrapper > div {
    display: inline-block;
    width: 150px;
    background-color: #90ee90;
    margin: 20px;
    padding: 10px;
  }
  #wrapper {
    display: flex;
    align-items: flex-start;
  }
</style>