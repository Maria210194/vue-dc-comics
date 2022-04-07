<template>
  <footer>
    <div class="container">
      <div class="links">
        <ul>
          <li><h3>DC Comics</h3></li>
          <li>Characters</li>
          <li>Comics</li>
          <li>Movies</li>
          <li>Tv</li>
          <li>Games</li>
          <li>Videos</li>
          <li>News</li>
        </ul>
        <ul>
          <li><h3>Shop</h3></li>
          <li>Shop DC</li>
          <li>Shop DC Collectibles</li>
        </ul>
        <ul>
          <li><h3>DC</h3></li>
          <li>Terms Of Use</li>
          <li>Privacy policy (New)</li>
          <li>Ad Choices</li>
          <li>Advertising</li>
          <li>Jobs</li>
          <li>Subscription</li>
          <li>Talent Workshops</li>
          <li>CPSC Certificates</li>
          <li>Ratings</li>
          <li>Shop Help</li>
          <li>Contact Us</li>
        </ul>
        <ul>
          <li><h3>Sites</h3></li>
          <li>DC</li>
          <li>MAD Magazine</li>
          <li>DC Kids</li>
          <li>DC Universe</li>
          <li>DC Power Visa</li>
        </ul>
      </div>
      <div class="bg-Dc"></div>
    </div>
    <div class="sign-up">sign up</div>
  </footer>
</template>

<script>
export default {
  name: "footerComponent",
};
</script>

<style scoped>
.container {
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
}

.links li {
  list-style-type: none;
}

.bg-Dc {
  width: 50%;
  height: 100%;
  position: absolute;
  background-image: url("../assets/dc-logo-bg.png");
  background-size: cover;
}
</style>