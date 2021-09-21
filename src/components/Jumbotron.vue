<template>
  <div>
      <img :src="require(`../assets/img/jumbotron.jpg`)" alt="">
  </div>
</template>

<script>
export default {
    name: 'Jumbo',
}
</script>

<style lang="scss" scoped>
div {
    height: 400px;
}
img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    object-position: 0 0 ;
}
</style>