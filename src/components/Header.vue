<template>
  <div class="header">
    <img src="../assets/img/dc-logo.png" alt="">
    <ul>
      <li :class="(link.current) ? 'active' : null" v-for="(link, index) in links" :key="index">
        <a :href="link.url">
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
@import "@/style/mixins";
.header {
  @include flex('spacearound');
  align-items: center;
  line-height: 100px;
  img {
    height: 80px;
  }
  ul{
    list-style: none;
    @include flex('center');
  }
  li {
    margin: 0 1rem;
  }
  li a {
    font-weight: 600;
    text-decoration: none;
    color: inherit;
    &:hover {
      color: $active;
      transition: color 0.5s;
    }
  }
  .active {
    color: $active;
    border-bottom: 2px solid;
  }
  
}
</style>
