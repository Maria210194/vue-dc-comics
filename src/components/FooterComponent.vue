<template>
  <footer>
    <div class="hero-footer">
      <div class="ms-container">
        <div>
          <h2>DC COMICS</h2>
          <ul>
            <li v-for="link in dcComicslLinks" :key="link.id">
              <a href="#">{{link.item}}</a>
            </li>
          </ul>
          <h2>SHOP</h2>
          <ul>
            <li>
              <a href="#">Shop DC</a>
            </li>
            <li>
              <a href="#">Shop DC Collectibles</a>
            </li>
          </ul>
        </div>

        <div>
          <h2>DC</h2>
          <ul>
            <li v-for="link in dcLinks" :key="link.id">
              <a href="#">{{link.item}}</a>
            </li>
          </ul>
        </div>

        <div>
          <h2>SITES</h2>
          <ul>
            <li v-for="link in sites" :key="link.id">
              <a href="#">{{link.item}}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import dcComicslLinks from '@/assets/data/FooterDCComics'
import dcLinks from '@/assets/data/FooterDCLinks'
import sites from '@/assets/data/FooterSitesLinks'

export default {
    name: 'FooterComponent',
    data() {
      return {
        dcComicslLinks,
        dcLinks,
        sites
      }
    }
}
</script>

<style lang="scss" scoped>
.hero-footer {
  background-image: url("@/assets/img/footer-bg.jpg");
  background-size: cover;
  // height: 400px;

  .ms-container {
    display: flex;
    // height: 400px;
    width: 80%;
    margin-inline: auto;
    gap: 1rem;
    padding: 3rem;
    background-image: url("@/assets/img/dc-logo-bg.png");
    background-repeat: no-repeat;
    background-position: right;
    background-size: 500px;

    h2 {
      color: white;
      font-size: 0.9rem;
      font-weight: 800;
      padding: 0.3rem 0;
      margin-left: 2rem;
    }

    ul {
      list-style: none;
      margin-bottom: 7px !important;

      li{
        line-height: 1.2rem;
      }

      a {
        color: #999;
        text-decoration: none;
        font-size: 0.7rem;
        
        &:hover {
          color: #008dff;
        }
      }
    }
  }
}
</style>