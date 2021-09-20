<template>
  <div>
    <div class="top">
      <h1> --> Content goes here &lt;-- </h1>
    </div>
    <div class="bottom">
      <ul>
        <li v-for="(link, index) in links" :key="index">
          <img src="../assets/img/buy-comics-digital-comics.png" :alt="link.text">
          <p>{{link.text}}</p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
// import * as Links from '@/assets/data/Links.js';
export default {
  name: 'Main',
  data() {
    return {
      links: [{
        imgUrl: 'buy-comics-digital-comics.png',
        text: 'digital comics'
    },
    {
        imgUrl: 'buy-comics-digital-merchandise.png',
        text: 'dc merchandise'
    },
    {
        imgUrl: 'buy-comics-digital-subscriptions.png',
        text: 'subscription'
    },
    {
        imgUrl: 'buy-comics-digital-locator.png',
        text: 'locator'
    },
    {
        imgUrl: 'buy-dc-power-visa.svg',
        text: 'DC power visa'
    },
]
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
  height: 200px;
  color: white;
  @include flex('start');
  padding: 1rem;
}
.bottom ul {
  @include flex('center');
  list-style: none;
  color: white;
  background-color: blue;
  text-transform: uppercase;
  li{
    @include flex('center'); 
    list-style: none;
    img {
        height: 4rem;
        padding: 1rem;
      }
  }
  
}
</style>
