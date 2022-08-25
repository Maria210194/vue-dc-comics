<template>
  <div class="comic-card">
      <img :src="img" :alt="title">
      <div class="details">
        <p class="type">{{ type }}</p>
        <h4 class="title">{{ title }}</h4>
      </div>
  </div>
</template>


<script>
export default {
    name: 'ComicCard',
    props: {
        img: String,
        title: String,
        type: String
    }
}
</script>


<style lang="scss" scoped>

.comic-card {
    flex-basis: calc(100% / 6 - 0.8rem * 5 / 6);
    position: relative;
    display: flex;
    flex-direction: column;

    img {
        width: 100%;
    }

    &:hover {
        img {
            transform: scale(1.1);
        }
        .title {
            color: #0075f9;
        }

    }

    .details{
        height: 90px;
        display: flex;
        flex-direction: column;
        align-items: self-start;

        .type {
            padding-top: 0.7rem;
            margin: 5px 0;
            font-size: 0.85rem;
            text-transform: uppercase;
            color: #0075f9;
        }

        .title{
            font-size: 1rem;
            text-transform: uppercase;
            word-break: break-word;
        }
    }
}
</style>