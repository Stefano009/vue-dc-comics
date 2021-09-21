<template>
  <div class="container">
      <div class="absolute">
          <h2>CURRENT SERIES</h2>
      </div>
      <ul>
          <li v-for="(comix, index) in cards" :key="index">
              <img :src="comix.thumb" alt="comix.series">
              <p>{{comix.series}}</p>
          </li>
      </ul>
      <button>
          LOAD MORE
      </button>
  </div>
</template>

<script>
import * as Comix from '@/assets/data/dc-comics.js'
export default {
    name: 'Cards',
    data() {
        return {
            cards: Comix.comix
        }
    }

}
</script>

<style lang="scss" scoped>
@import "@/style/mixins";
.container {
    position: relative;
    flex-direction: column;
    @include flex('center');
    height:600px;

}
ul {
    width: 75%;
    margin: 0 auto;
    display: flex;
    flex-wrap: wrap;
    flex-basis: fit-content;
    li {
        width: calc((100% / 6) - 1rem);
        list-style: none;
        padding: .5rem;
    }
    img {
        padding: 1rem;
        height: 200px;
        width: 200px;
        object-fit: cover;
        object-position: 0 0;
    }
    p{
        width: 200px;
        font-size: .8rem;
    }
}
button {
    background-color: #0282F9;
    color: white;
    padding: .5rem 2rem;
    margin-top: 4rem;
}
.absolute {
    background-color: #0282F9;
    position: absolute;
    top: 0;
    left: 16rem;
    transform: translateY( -100%);
    padding: .6rem 1.5rem;
    font-size: 1.2rem;
}
</style>
