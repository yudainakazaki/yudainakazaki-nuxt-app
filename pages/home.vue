<script setup lang="ts">
import { onMounted } from 'vue';

</script>

<template>
  <div class="home">
    <div class="home__main">
        <img src="../../public/images/yudainakazaki.png" class="home__main__name">
        <img src="../../public/images/top.png" alt="name" class="home__main__profile">
        <img src="../../public/images/yudainakazaki_black.png" class="home__main__name-mobile" />
    </div>
    <div class="home__sub">
      <p class="home__sub__description font-serif">
        I am Yudai, <br>
        who loves making something beautiful and making people laugh :D <br>
        <span class="spacer"/>
        I am originally from Tokyo and currently live in Amsterdam. <br>
        <span class="spacer"/>
        My interest is in Software Engineering, Natural Language Processing, Theory of Comedy, etc.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>

.home {
  min-height: calc(100vh - 180px);

  &__main {
    position: relative;
    display: block;
    margin-left: auto;
    width: 66.8%;

    &__name {
      position: absolute;
      top: 35%;
      left: -40%;
      width: 69.5%;
      animation: 2s ease-in 0s showUp;
      transform-origin: left;
    }

    &__name-mobile {
      display: none;
    }

    &__profile {
      width: 100%;
      animation: 1s ease-out loadImage;
    }
  }

  &__sub {
    width: 55%;
    margin: 64px auto;

    &__description {
      font-size: 24px;
      font-weight: 500; 
      margin: 64px;
      line-height: 2;
    }
  }
}

@media (max-width: 976px) {
  .home {
    &__main {
      display: flex;
      flex-direction: column;
      width: 100%;

      &__name {
        display: none;
      }

      &__name-mobile {
        margin: 36px auto;
        display: block;
        position: relative;
        width: 70%;
        animation: 2s ease-in 0s showUp;
        transform-origin: left;
      }

      &__profile {
        width: 100%;
        animation: 1s ease-out loadImage;
      }
    }

    &__sub {
      width: 90%;
      margin: auto;

      &__description {
        font-size: 18px;
        font-weight: 500; 
        margin: 0 64px;
        line-height: 2;
      }
    }
  }
}

@keyframes loadImage {
  0% {
    transform: scale(1.1);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes showUp {
  0% {
    opacity: 0;
  }
  45% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
