<template>
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
  @include flex('spacearound');
  align-items: center;
  width: 100%;
  height: 560px;
  margin: 0 auto;
  img {
      height: 600px;
      object-fit: contain;
      overflow: hidden;
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
</style>
