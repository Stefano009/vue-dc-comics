<template>
  <div class="header">
    <img src="../assets/img/dc-logo.png" alt="">
    <ul>
      <li :class="(link.current) ? 'active' : null" v-for="(link, index) in links" :key="index">
        <a :href="links.url">
          {{ link.text }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
import * as Links from '@/assets/data/Links.js';
export default {
  name: 'Header',

  data() {
    return {
      links: Links.headerLinks
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "@/style/signatureColors";
.header {
  display: flex;
  justify-content: space-around;
  align-items: center;
  line-height: 100px;
  img {
    height: 80px;
  }
  ul{
    list-style: none;
  }
  li {
    display: inline-block;
    margin: 0 1rem;
  }
  a {
    font-weight: 600;
  }
  .active {
    color: $active;
    border-bottom: 2px solid;
  }
}
</style>
