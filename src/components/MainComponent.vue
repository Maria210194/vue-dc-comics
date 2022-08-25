<template>
  <div class="main-body">
    <div class="hero">
        <div class="container">
          <div class="active-series">
            current series
          </div>
        </div>
    </div>
    <div class="container">
      <div class="comics">
        <ComicCard v-for="card in dcComics" :key="card.series" :img="card.thumb" :title="card.series" :type="card.type"/>
      </div>
      <div class="more">
        <button type="button">load more</button>
      </div>
    </div>
  </div>
</template>

<script>
import dcComics from '@/assets/data/dc-comics';
import ComicCard from './ComicCard.vue';


export default {
    name: "MainComponent",
    data() {
      return {
        dcComics
      }
    },
      components: { 
        ComicCard
      }
}
</script>

<style scoped lang="scss">

.main-body {
  color: white;
  background: #1c1c1c;
  .hero {
    height: 20rem;
    background-image: url("@/assets/img/jumbotron.jpg");
    background-position: top;
    background-size: cover;
    position: relative;
    .active-series {
      position: absolute;
      transform: translateY(50%);
      bottom: 0;
      text-transform: uppercase;
      font-size: 0.9rem;
      font-weight: 900;
      padding: 0.5rem 1rem;
      border-radius: 1px;
      background-color: #0282f9;
    }
  }
  .comics {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
    padding: 3rem 0;
  }
  .more {
    padding: 1rem 0;
    text-transform: uppercase;
    text-align: center;
    button {
      border: none;
      border-radius: 1px;
      color: white;
      font-size: 0.8rem;
      font-weight: 700;
      padding:  0.5rem 1.5rem;
      margin-bottom: 10px;
      background: #0282f9;
      transition: 0.3s;
      cursor: pointer;
      &:hover {
          box-shadow: inset 0px 0px 0 2px;
          border-radius: 5px;
      }
    }
  }
}

</style>