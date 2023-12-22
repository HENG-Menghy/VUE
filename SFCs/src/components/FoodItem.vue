<template>
  <div>
    <h2>
      {{ footName }}
      <img src="/img_quality.svg" v-show="isFavorite">
    </h2>
    <p>{{ Desc }}</p>
  </div>
</template>

<script>
  export default {
    props: ['footName', 'Desc', 'isFavorite']
  }
</script>

<style scoped> 
  img {
    float: right;
    height: 1.5rem;
  }
</style>