<template>
  <div id="app">
    <FirstScroll />
    <SecondScroll />
    <ThirdScroll />
    <FourthScroll />
    <FifthScroll />
    <SixthScroll />
    <modals-container />
    <Preloader v-if="preloader"/>
  </div>
</template>

<script>
/* eslint-disable */
import FirstScroll from './components/FirstScroll.vue'
import SecondScroll from './components/SecondScroll.vue'
import ThirdScroll from './components/ThirdScroll.vue'
import FourthScroll from './components/FourthScroll.vue'
import FifthScroll from './components/FifthScroll.vue'
import SixthScroll from './components/SixthScroll.vue'
import Preloader from './components/Preloader/Preloader.vue'

export default {
  name: 'app',
  components: {
    FirstScroll,
    SecondScroll,
    ThirdScroll,
    FourthScroll,
    FifthScroll,
    SixthScroll,
    Preloader
  },
  data() {
    return {
      preloader: true,
    }
  },
  mounted() {
    setTimeout(() => {
      this.preloader = false
    }, 1500)
  }
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css?family=Questrial');
  #app {
    font-family: "Questrial", sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    margin: 0;
    position: relative;
    overflow: hidden;
  }
  body {
    font-family: 'Questrial', sans-serif;
    margin: 0;
  }
  .wrapper {
    width: 100%;
    display: block;
  }
  .layout {
    max-width: 1170px;
    width: 100%;
    display: block;
    margin: auto;
    z-index: 2;
    position: relative;
  }
  .title {
    font-size: 60px;
    line-height: 55px;
    font-weight: 300;
    margin: 50px 0 0 0;
  }
  .percent-text {
    display: none;
  }
  .descr {
    font-size: 22px;
    line-height: 22px;
    font-weight: 500;
    margin: 20px 0 0 0;
  }
  .VueCarousel-wrapper {
    max-width: 1035px;
    overflow: hidden;
    margin: auto;
  }
  .VueCarousel-inner {
    margin: 50px auto 0;
    display: flex;
    align-items: center;
  }
  .VueCarousel-navigation-button {
    top: 38% !important;
  }
  .VueCarousel-navigation-prev, .VueCarousel-navigation-next {
    outline: none !important;
    width: 37px !important;
    height: 37px !important;
    display: block !important;
    -webkit-border-radius: 50% !important;
    -moz-border-radius: 50% !important;
    border-radius: 50% !important;
    background-color: #e8effb !important;
    opacity: .5;
    transition: .3s;
    cursor: pointer;
    &:hover {
      opacity: .7;
      transition: .3s;
    }
    &:active {
      opacity: 1;
      transition: .3s;
    }
  }
  .VueCarousel-navigation-next {
    background-image: url("assets/img/buttonRight.svg");
    right: 55px !important;
  }
  .VueCarousel-navigation-prev {
    background-image: url("assets/img/button.svg");
    left: 55px !important;
  }

  .VueCarousel-pagination {
    display: none;
  }
  .v--modal-overlay .v--modal-background-click {
    background-color: #ffffff75 !important;
  }
  .v--modal {
    height: fit-content !important;
    width: 600px !important;
    top: calc(50% - 300px) !important;
  }
  @media (max-width: 768px), (max-height: 420px) {
    .VueCarousel-inner {
      margin: 30px auto 0;
    }
    .v--modal {
      width: 90% !important;
      margin: auto;
      top: calc(40% - 200px) !important;
    }
    .v--modal-box .v--modal {
      width: 90% !important;
      left: 0 !important;
      right: 0 !important;
      margin: auto !important;
    }
    .close {
      top: 15px !important;
      right: 15px !important;
      & > img {
        width: 30px;
      }
    }
    .button {
      font-size: 14px !important;
    }
    .VueCarousel-navigation-next {
      right: 45px !important;
    }
    .VueCarousel-navigation-prev {
      left: 45px !important;
    }
  }
</style>
