<template>
  <ul>
    <todoItem
    v-for="item in items"
    :key="item"
    :itemName="item"
    id="lightgreen"
    style="background-color: #90ee90;"
    />
  </ul>
  <input type="text" v-model="inputVal" @keydown.enter="addItem">
  <button @click="addItem">Add</button>
</template>
<script>
  export default {
    data() {
      return {
        items: ['Apple', 'Rice', 'Sandwich', 'Cake'],
        inputVal: ''
      }
    },
    methods: {
      addItem() {
        this.items.push(this.inputVal)
        this.inputVal = ''
      }
    }
  }
</script>
<style scoped>
  ul {
    width: 150px;
    list-style-type: none;
    padding-left: 10px;
  }
</style>