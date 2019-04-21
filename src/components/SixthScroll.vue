<template>
    <div id="footer-scroll" class="wrapper sixth-scroll">
        <div class="layout background-sixth">
            <div class="background-sixth-scroll">
                <div :class="{ 'animate-tree-one':animationValue}"  class="background-sixth-scroll__tree-right background-style"></div>
                <div :class="{ 'animate-tree-one':animationValue}" class="background-sixth-scroll__tree-left background-style"></div>
                <div class="background-sixth-scroll__hips-one background-style"></div>
                <div class="background-sixth-scroll__hips-two background-style"></div>
                <div class="background-sixth-scroll__phones background-style"></div>
                <div :class="{ 'move-man-one':animationValue}" class="background-sixth-scroll__man-one background-style"></div>
                <div :class="{ 'move-man-one':animationValue}" class="background-sixth-scroll__man-two background-style"></div>
                <div :class="{ 'move-man-two':animationValue}" class="background-sixth-scroll__man-three background-style"></div>
                <div :class="{ 'bush-animation':animationValue}" class="background-sixth-scroll__bush background-style"></div>
                <div class="background-sixth-scroll__city background-style"></div>
                <div class="background-sixth-scroll__city-two background-style"></div>
            </div>
            <h1 class="heading__title title">Free Download</h1>
            <div class="heading__buttons">
                <DownloadButtons />
            </div>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
  import DownloadButtons from './DownloadButtons'

  export default {
    name: "SixthScroll",
    components: {
      DownloadButtons,
    },
    data() {
      return {
        scrolled: 0,
        currentScroll: 0,
        animationValue: false,
      }
    },
    created () {
      window.onscroll = this.handleScroll
    },
    methods: {
      handleScroll() {
        this.scrolled = Math.floor(window.pageYOffset)
        this.currentScroll = Math.floor(document.getElementById('footer-scroll').offsetTop)
      },
    },
    watch: {
      'scrolled'(value) {
        if (value > this.currentScroll) {
          this.animationValue = true
        } else {
          this.animationValue = false
        }
      }
    },
  }
</script>

<style scoped lang="scss">
    .background-sixth {
        padding: 150px 0;
        height: 1400px;
        box-sizing: border-box;
        display: flex;
        align-items: center;
        flex-direction: column;
        position: relative;
    }
    .background-style {
        position: absolute;
        display: block;
        background-position: center;
        background-size: contain;
        background-repeat: no-repeat;
    }
    .background-sixth-scroll {
        &__tree-left {
            width: 277px;
            height: 420px;
            top: 35%;
            left: 100px;
            z-index: 2;
            background-image: url("../assets/img/tree-left.png");
        }
        &__tree-right {
            width: 250px;
            height: 412px;
            top: 40%;
            right: 0;
            z-index: 2;
            background-image: url("../assets/img/tree.png");
        }
        &__hips-one {
            width: 100%;
            height: 80px;
            left: 0;
            top: 50%;
            background-image: url("../assets/img/horizont.png");
        }
        &__phones {
            width: 900px;
            height: 650px;
            top: calc(60% - 325px);
            left: calc(50% - 450px);
            background-image: url("../assets/img/phones.png");
        }
        &__hips-two {
            width: 100%;
            height: 80px;
            left: 0;
            top: 50%;
            background-image: url("../assets/img/horizont2.png");
        }
        &__city-two {
            width: 300px;
            height: 350px;
            top: 27%;
            right: 100px;
            z-index: -1;
            background-image: url("../assets/img/city-two.png");
        }
        &__city {
            width: 300px;
            height: 350px;
            top: 30%;
            left: 100px;
            z-index: -1;
            background-image: url("../assets/img/city.png");
        }
        &__man-one {
            width: 180px;
            height: 320px;
            top: 50%;
            left: 0;
            z-index: 3;
            background-image: url("../assets/img/footer-man2.png");
        }
        &__man-two {
            width: 240px;
            height: 340px;
            top: 60%;
            left: 200px;
            z-index: 3;
            background-image: url("../assets/img/footer-man3.png");
        }
        &__man-three {
            width: 240px;
            height: 370px;
            top: 60%;
            right: 200px;
            z-index: 3;
            background-image: url("../assets/img/footer-man.png");
        }
        &__bush {
            background-image: url('../assets/img/bush.png');
            background-position: bottom right;
            background-size: contain;
            height: 280px;
            width: 1300px;
            right: -600px;
            bottom: 0;
            z-index: 5;
        }
    }

    .animate-tree-one {
        animation: animate-tree-one 2s ease forwards;
    }

    .move-man-one {
        animation: move-man-one 3s ease-in-out forwards;
    }
    .move-man-two {
        animation: move-man-two 3s ease-in-out forwards;
    }

    .bush-animation {
        animation: bush-animation 2s ease-out forwards;
    }

    @keyframes animate-tree-one {
        0% {
            margin: 0;
        }
        100% {
            margin: -50px 0 0 0;
        }
    }

    @keyframes move-man-one {
         0% {
             margin: 0;
         }
         100% {
             margin: 0 0 0 60px;
         }
     }

    @keyframes move-man-two {
        0% {
            margin: 0;
        }
        100% {
            margin: 0 40px 0 0;
        }
    }
    @keyframes bush-animation {
        0% {
            bottom: -20px;
            right: -620px;
        }
        100% {
            bottom: 0;
            right: -600px;
        }
    }
</style>
