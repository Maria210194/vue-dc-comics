<template>
  <div class="bottom-footer">
      <div class="container">
        <div class="action">
          <button type="button">SIGN-UP NOW!</button>
        </div>
        <div class="contacts">
          <h2>FOLLOW US</h2>
          <ul class="menu">
            <li v-for="image in images" :key="image.id">
              <a href="#">
                <img :src="image.src" :alt="image.name">
              </a>
            </li>
          </ul>       
        </div>
      </div>
    </div>
</template>

<script>
export default {
    name: 'BottomFooter', 
    data() {
      return {
        images: [
          {          
            src: require("@/assets/img/footer-facebook.png"),
            name: "facebook",
            id: 0
          },
                    {          
            src: require("@/assets/img/footer-twitter.png"),
            name: "twitter",
            id: 1
          },
                    {          
            src: require("@/assets/img/footer-youtube.png"),
            name: "youtube",
            id: 2
          },
                    {          
            src: require("@/assets/img/footer-pinterest.png"),
            name: "ointerest",
            id: 3
          },
                    {          
            src: require("@/assets/img/footer-periscope.png"),
            name: "periscope",
            id: 4
          },
        ]
      }
    }

}
</script>

<style lang="scss" scoped>
.bottom-footer {
  background: #303030;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 0;
  }

  button {
    padding: 0.6rem;
    background: none;
    color: white;
    font-weight: 600;
    cursor: pointer;
    border: 2px solid #008dff;
    border-radius: 2px;
    &:hover {
      background: #008dff;
      color: #303030;
    }
  }

  .contacts {
    display: flex;
    align-items: center;
    gap: 1rem;
    h2 {
      color: #008dff;
      font-size: 1rem;
      margin: 0;
    }

    ul{
      margin: 0;
    }

    .menu {
      list-style: none;
      display: flex;
      align-items: center;
      gap: 1rem;
      a {
        display: flex;
      }
      img {
        height: 1.8rem;
        &:hover {
          opacity: 0.4;
        }
      }
    }
  }
}
</style>