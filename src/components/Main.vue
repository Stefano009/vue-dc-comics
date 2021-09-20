<template>
  <div>
    <div class="top">
      <h1> --> Content goes here &lt;-- </h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Main',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/signatureColors";
@import "@/style/mixins";
.top {
  background-color: $topMain;
  height: 200px;
  color: white;
  @include flex('start');
  padding: 1rem;
}
</style>
