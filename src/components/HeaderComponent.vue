<template>
<header>
    <div class="ms-container container-fluid">
        <div class="header-logo">
          <a href="#">
            <img src="@/assets/img/dc-logo.png" alt="DC-logo">
          </a>
        </div>
        <nav>
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
  &::before {
    position: absolute;
    content: "";
    width: 100%;
    height: 3px;
    top: 4rem;
    padding: 0 5px;
    background: #0282f9;
    transform: scaleY(0);
    transform-origin: left;
    transition: transform 0.2s ease-in;
  }
  &:hover::before {
    transform: scaleY(1);
  }
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