<template>
  <div class="bottom-footer">
      <div class="container">
        <div class="action">
          <button type="button">SIGN-UP NOW!</button>
        </div>
        <div class="contacts">
          <h2>FOLLOW US</h2>
          <ul class="menu">
            <li>
              <a href="#">
                <img src="@/assets/img/footer-facebook.png" alt="facebook">
              </a>
            </li>
            <li>
              <a href="#">
                <img src="@/assets/img/footer-twitter.png" alt="twitter">
              </a>
            </li>
            <li>
              <a href="#">
                <img src="@/assets/img/footer-youtube.png" alt="youtube">
              </a>
            </li>
            <li>
              <a href="#">
                <img src="@/assets/img/footer-pinterest.png" alt="pinterest">
              </a>
            </li>
            <li>
              <a href="#">
                <img src="@/assets/img/footer-periscope.png" alt="periscope">
              </a>
            </li>
          </ul>       
        </div>
      </div>
    </div>
</template>

<script>
export default {
    name: 'BottomFooter'

}
</script>

<style lang="scss" scoped>
.bottom-footer {
  background: #303030;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.5rem 0;
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
    }
  }

  .contacts {
    display: flex;
    align-items: center;
    gap: 1rem;
    h2 {
      color: #008dff;
      font-size: 1rem;
    }
    .menu {
      list-style: none;
      display: flex;
      align-items: center;
      gap: 1rem;
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