<template>
  <div>
    <div class="footer">
      <ul class="outer-list">
        <li :class="(link.current) ? 'active' : null" v-for="(link, index) in links" :key="index">
          <h3>{{link.title}}</h3>
          <ul>
            <li v-for="(data, index ) in links[index].data" :key="index">
              <a :href="link.url">
                {{ data.text }}
              </a>
            </li>
          </ul>
        </li>
      </ul>
      <img src="../assets/img/dc-logo-bg.png" alt="">
    </div>
    <div class="bottom-footer">
      <button>
        SIGN-UP NOW!
      </button>
      <div class="socials">
        <h2>FOLLOW US</h2>
        <img src="../assets/img/footer-facebook.png" alt="facebook">
        <img src="../assets/img/footer-twitter.png" alt="twitter">
        <img src="../assets/img/footer-youtube.png" alt="youtube">
        <img src="../assets/img/footer-pinterest.png" alt="pinterest">
        <img src="../assets/img/footer-periscope.png" alt="periscope">
      </div>
    </div>
  </div>
</template>

<script>
import * as Links from '@/assets/data/Links.js';
export default {
  name: 'Footer',
  data() {
    return {
      links: Links.footerLinks
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/signatureColors";
@import "@/style/mixins";
.footer {
  background-image: url('../assets/img/footer-bg.jpg');
  background-size: cover;
  @include flex('spacearound');
  align-items: center;
  width: 100%;
  height: 400px;
  margin: 0 auto;
  object-fit: contain;
  overflow: hidden;
  img {
      height: 600px;
      
    }
  .outer-list {
    ul {
      padding: 0;
    }
    @include flex('column');
    height: 300px;
    width: 30%;
    list-style-type: none;
    padding: 0;
    li {
      list-style-type: none;
      text-align: start;
      color: white;
    }
  }
}
.bottom-footer {
  color: gray;
  @include flex('spacearound');
  align-items: center;
  background-color: #303030;
  height: 80px;
  button {
    height: 2rem;
    padding: 0.3rem;
    background-color: #303030;
    color: white;
    border-style: none;
    border:2px solid #0282F9;
    
  }
  .socials {
    h2 {
      color: #0282F9;
      font-size: 1.2rem
    }
    @include flex();
    align-items: center;
    img {
    padding: 0 .5rem;
    height: 1.5rem;
    }
  }
  
}
</style>
