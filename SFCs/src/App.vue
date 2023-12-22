<template>
  <h1>Food</h1>
  <div id="wrapper">
    <foot-item 
    footName="Apple"
    Desc="Apple is a type of fruit that grow on tree."
    v-bind:isFavorite="false"/>
    <foot-item
    footName="Pizza"
    Desc="Pizza has a bread base with tomato sauce, cheese, and toppings on top."
    v-bind:isFavorite="false"/>
    <foot-item
    footName="Rice"
    Desc="Rice is a type of grain that people like to eat."
    v-bind:isFavorite="false"/>
    <foot-item
    footName="Soup"
    Desc="I like to eat soup so much."
    v-bind:isFavorite="true"/>
    <foot-item
    footName="Ice Late Coffee"
    Desc="I want to drink it all a single day."
    v-bind:isFavorite="true"/>
  </div>
</template>

<script> </script>

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