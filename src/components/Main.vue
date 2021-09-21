<template>
  <div>
    <div class="top">
          <Cards />
    </div>
    <div class="bottom">
      <ul>
        <li v-for="({img, text}, index) in link" :key="index">
          <!-- <h1>{{img}}</h1>00 -->
          <img :src="require(`../assets/img/${img}`)" :alt="text">
          <p>{{text}}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import * as Links from '@/assets/data/Links.js';
import Cards from '@/components/Cards.vue'
export default {
  name: 'Main',
  components: {
    Cards,
  },
  data() {
    return {
      link: Links.mainLinks 
    }
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/signatureColors";
@import "@/style/mixins";
.top {
  background-color: $topMain;
  color: white;
  @include flex('start');
  padding: 1rem;
}
.bottom ul {
  @include flex('center');
  list-style: none;
  height: 150px;
  color: white;
  background-color: #0282F9;
  text-transform: uppercase;
  li{
    @include flex('center'); 
    list-style: none;
    padding: 3rem;
    img {
        height: 4rem;
        
      }
  }
  
}
</style>
