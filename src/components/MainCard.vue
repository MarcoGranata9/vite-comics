<script>
export default {
  props: {
    title: String,
    image: String,
  }
}
</script>

<template>
  <div class="card">
    <img :src="image" :alt="title">
    <h3>{{ title }}</h3>         
  </div>
</template>

<style lang="scss" scoped>
.card{
  color: white;

  img {
    width: 200px;
    height: 200px;
    margin-bottom: 10px;
  }
}
</style>