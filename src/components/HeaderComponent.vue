<template>
<header>
    <div class="ms-container container-fluid">
        <div class="header-logo">
          <a href="#">
            <img src="@/assets/img/dc-logo.png" alt="DC-logo">
          </a>
        </div>
        <nav class="cl-effect-12">
          <ul class="items">
            <li v-for="link in HeaderItems" :key="link.id" :class="link.active ? 'active' : '' ">
              <a href="#"> {{ link.item }} </a>
            </li>
          </ul>
        </nav>
    </div>
    </header>
</template>

<script>
import HeaderItems from '@/assets/data/HeaderItems'

export default {
  name: 'HeaderComponent',
  data() {
      return {
          HeaderItems,
      }
  }

}
</script>

<style scoped lang="scss">

.ms-container {
  display: flex;
  align-items: center;
  justify-content: space-around;

  .cl-effect-12 a::before,
  .cl-effect-12 a::after {
    position: absolute;
    top: 50%;
    left: 50%;
    width: 80px;
    height: 80px;
    border: 2px solid rgba(0,0,0,0.1);
    border-radius: 50%;
    content: '';
    opacity: 0;
    -webkit-transition: -webkit-transform 0.3s, opacity 0.3s;
    -moz-transition: -moz-transform 0.3s, opacity 0.3s;
    transition: transform 0.3s, opacity 0.3s;
    -webkit-transform: translateX(-50%) translateY(-50%) scale(0.2);
    -moz-transform: translateX(-50%) translateY(-50%) scale(0.2);
    transform: translateX(-50%) translateY(-50%) scale(0.2);
  }

  .cl-effect-12 a::after {
    width: 70px;
    height: 70px;
    border-width: 6px;
    -webkit-transform: translateX(-50%) translateY(-50%) scale(0.8);
    -moz-transform: translateX(-50%) translateY(-50%) scale(0.8);
    transform: translateX(-50%) translateY(-50%) scale(0.8);
  }

  .cl-effect-12 a:hover::before,
  .cl-effect-12 a:hover::after,
  .cl-effect-12 a:focus::before,
  .cl-effect-12 a:focus::after {
    opacity: 1;
    -webkit-transform: translateX(-50%) translateY(-50%) scale(1);
    -moz-transform: translateX(-50%) translateY(-50%) scale(1);
    transform: translateX(-50%) translateY(-50%) scale(1);
  }
}

img {
  width: 4.5rem;
  padding: 10px 0;
}

.items {
  list-style-type: none;
  display: flex;
  gap: 0.5rem;
  position: relative;
  
  a{
    padding: 0 10px;
    color: #2c3e50;
    text-decoration: none;
    text-transform: uppercase;
    font-size: 0.7rem;
    font-weight: bolder;
    &:hover {
      color: #0282f9;
    }
  }
}

li {
  position: relative;
}

.active {
  a {
    color: #0282f9;
  }
  &::before {
    transform: scaleY(1);
  }
}

</style>