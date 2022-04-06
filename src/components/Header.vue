<template>
  <header>
    <div>
      <img src="../assets/dc-logo.png" alt="DC logo" />
    </div>
    <div>
      <nav></nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style scoped>
header img {
  width: 60px;
  height: 60px;
  margin: 10px;
}

nav {
  width: 50%;
}
</style>