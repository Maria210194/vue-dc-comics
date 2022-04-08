<template>
  <footer>
    <div class="top-header">
      <div class="links col-5 container-fluid">
        <ul>
          <li><h3>DC Comics</h3></li>
          <li><a href="#">Characters</a></li>
          <li><a href="#">Comics</a></li>
          <li><a href="#">Movies</a></li>
          <li><a href="#">TV</a></li>
          <li><a href="#">Games</a></li>
          <li><a href="#">Videos</a></li>
          <li><a href="#">News</a></li>
        </ul>
        <ul>
          <li><h3>Shop</h3></li>
          <li><a href="#">Shop DC</a></li>
          <li><a href="#">Shop DC Collectibles</a></li>
        </ul>
        <ul>
          <li><h3>DC</h3></li>
          <li><a href="#">Terms Of Use</a></li>
          <li><a href="#">Privacy policy (New)</a></li>
          <li><a href="#">Ad Choices</a></li>
          <li><a href="#">Advertising</a></li>
          <li><a href="#">Jobs</a></li>
          <li><a href="#">Subscriptions</a></li>
          <li><a href="#">Talent WorkShops</a></li>
          <li><a href="#">CPSC Certificates</a></li>
          <li><a href="#">Ratings</a></li>
          <li><a href="#">Shop Help</a></li>
          <li><a href="#">Contact Us</a></li>
        </ul>
        <ul>
          <li><h3>Sites</h3></li>
          <li><a href="#">DC</a></li>
          <li><a href="#">MAD Magazine</a></li>
          <li><a href="#">DC Kids</a></li>
          <li><a href="#">DC Universe</a></li>
          <li><a href="#">DC Power Visa</a></li>
        </ul>
      </div>
      <div class="bg-Dc col-sm-7">
        <img src="@/assets/dc-logo-bg.png" alt="DC" />
      </div>
    </div>
    <div class="sign-up"><a href="#">SIGN-UP NOW</a></div>
  </footer>
</template>


<script>
export default {
  name: "footerComponent",
};
</script>



<style lang="scss" scoped>
@import "variables";

.top-header {
  background-image: url("../assets/footer-bg.jpg");
  display: flex;
  justify-content: space-around;
  position: relative;
  height: 200px;
}

.links {
  display: flex;
  flex-wrap: wrap;
  color: white;
  font-size: 8px;
  width: 50%;

  li {
    list-style-type: none;

    a {
      color: $link-color;
      text-decoration: none;
    }
  }
}

.bg-Dc {
  width: 80px;
  height: 80px;
}
</style>