<template>
  <div class="bottom-footer">
      <div class="container">
        <div class="action">
          <button type="button" class="sign-up">sign-up now!</button>
        </div>
        <div class="contacts">
          <a href="https://www.dcuniverseinfinite.com/" class="follow">follow us</a>
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

    .action{
      text-transform: uppercase;
    }
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
    
    .follow {
      color: #008dff;
      font-size: 1rem;
      text-transform: uppercase;
      margin: 0;
      cursor: pointer;
    }

    ul{
      margin: 0;
    }

    .menu {
      display: flex;
      gap: 1rem;
      align-items: center;
      list-style: none;
      
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