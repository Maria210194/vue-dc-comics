<template>
  <main>
    <div class="container-fluid">
      <div class="content">Content goes here!</div>
      <div class="icons">ICONS</div>
    </div>
  </main>
</template>

<script>
export default {
  name: "mainComponent",
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
}

.content {
  width: 100%;
  background-color: black;
  color: white;
  height: 180px;
}

.icons {
  width: 100%;
  background-color: #0282f9;
  color: white;
  height: 180px;
}
</style>