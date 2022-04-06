<template>
  <header>
    <div>
      <img src="../assets/dc-logo.png" alt="DC logo" />
    </div>
    <div>
      <nav>
        <ul>
          <li>Characters</li>
          <li>Comics</li>
          <li>Movies</li>
          <li>Tv</li>
          <li>Games</li>
          <li>Collectibles</li>
          <li>Videos</li>
          <li>Fans</li>
          <li>News</li>
          <li>Shop</li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-around;
}
header img {
  width: 60px;
  height: 60px;
  margin: 10px;
}

nav {
  width: 50%;
}

ul {
  display: flex;
  padding-top: 20px;
}

ul li {
  list-style-type: none;
  text-transform: uppercase;
  padding: 5px;
  font-size: 11px;
}
</style>