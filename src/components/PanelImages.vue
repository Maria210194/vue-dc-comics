<template>
  <div class="panel-images">
    <div class="container">
      <ul class="logo-images">
        <li v-for="image in images" :key="image.name">
          <a href="#">
            <img :src="image.src" alt="digital-comics">
            <span>{{image.name}}</span>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>

export default {
  name: 'PanelImages',
  data() {
    return {
      images: [
      {
          src: require("@/assets/img/buy-comics-digital-comics.png"),
          name: "digital comics"
      }, 
      {
          src: require("@/assets/img/buy-comics-merchandise.png"),
          name: "dc merchandise"
      }, 
      {
          src: require("../assets/img/buy-comics-subscriptions.png"),
          name: "subscription"
      }, 
      {
          src: require("../assets/img/buy-comics-shop-locator.png"),
          name: "comic shop locator"
      }, 
      {
          src: require("@/assets/img/buy-dc-power-visa.svg"),
          name: "dc power visa"
      }
      ]
    }
  }
}
</script>

<style scoped lang="scss">


.panel-images {
  background: #0282f9;
  height: 100px;
}
.logo-images {
  list-style: none;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 1.2rem 0;
  li:last-child {
    height: 3.5rem;
    display: flex;
    img {
      height: 1.7rem;
    }
  }
  li {
    border: 0.5rem solid transparent;
    border-radius: 50px;
    padding: 0 10px;
    &:hover {
      background-color: rgba(244, 241, 241, 0.1);
    }
  }
  a {
    color: white;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 0.7rem;
    font-weight: 400;
    display: flex;
    align-items: center;
    gap: 0.7rem;
    img {
      height: 2.5rem;
    }
  }
}
</style>
