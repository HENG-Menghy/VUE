<template>
  <h1>Example v-for-Component</h1>
  <p>Click Favorite button to show and also hidden image.</p>
  <button @click="removeItem">Remove Item</button>
  <div id="wrapper">
    <food-item
    v-for="food in Foods"
    :key="food.name"
    :foodName="food.name"
    :foodDesc="food.desc"
    :isFavorite="food.favorite"
    @toggle-favorite="recieveEmit"
    />
  </div>
</template>
<script>
  export default {
    data() {
      return {
        Foods: 
        [
          {
            name: 'Apples',
            favorite: true
          },
          {
            name: 'Rice',
            desc: 'Rice are type of energy food. People like to eat it.',
            favorite: false
          },
          {
            name: 'Hot Soup',
            desc: 'The hot soup is yummy. It is hot and good for eating.',
            favorite: true,
            bgColor: '#f2f2f2'
          },
          {
            name: 'Pizza',
            desc: "Pizza are type of fast food. Most of people like to eat it, but it doesn't for health",
            favorite: false
          }
        ]
      }
    },
    methods: {
      recieveEmit(food) {
        const foundFood = this.Foods.find(isFood => isFood.name === food);
        foundFood.favorite = !foundFood.favorite
      },
      removeItem() {
        this.Foods.splice(1,1)
      }
    }
  }
</script>
<style scoped>

</style>