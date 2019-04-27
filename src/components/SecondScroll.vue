<template>
    <div id="second-scroll" class="wrapper second-scroll">
        <div class="layout layout-second-scroll">
            <div class="options-container">
                <h1 v-if="circleWidth === 400" class="options-container__heading title">How it works</h1>
                <div id="third-scroll" class="options" @click="updateProgress(25, 1)">
                    <div :class="{ 'active-description': isFirstDescription }" class="options__wrapper">
                        <img class="icon" v-if="isFirstDescription" src="../assets/img/eye-icon-active.svg" />
                        <img class="icon" v-else src="../assets/img/eye-icon.svg" />
                        <div class="options__descr">
                            <h3 :class="{ 'active-description': isFirstDescription }" class="options__name">How it works</h3>
                            <p v-if="isFirstDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
                <div class="options" @click="updateProgress(50, 2)">
                    <div :class="{ 'active-description': isSecondDescription }" class="options__wrapper">
                        <img class="icon" v-if="isSecondDescription" src="../assets/img/point-icon-active.svg" />
                        <img class="icon" v-else src="../assets/img/point-icon.svg" />
                        <div class="options__descr">
                            <h3 :class="{ 'active-description': isSecondDescription }" class="options__name">Friends</h3>
                            <p v-if="isSecondDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
                <div class="options" @click="updateProgress(75, 3)">
                    <div :class="{ 'active-description': isThirdDescription }" class="options__wrapper">
                        <img class="icon" src="../assets/img/smile-icon-active.svg" v-if="isThirdDescription" />
                        <img class="icon" src="../assets/img/smile-icon.svg" v-else />
                        <div class="options__descr">
                            <h3 :class="{ 'active-description': isThirdDescription }" class="options__name">Travel</h3>
                            <p v-if="isThirdDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="circle">
                <div class="empty-fill"></div>
                <span
                      :class="{ active: currentProgress > 0 }"
                      class="circle__point-one circle__point">
                </span>
                <span
                      :class="{ active: currentProgress > 25 }"
                      class="circle__point-two circle__point">
                </span>
                <span
                      :class="{ active: currentProgress > 50 }"
                      class="circle__point-three circle__point">
                </span>
                <span
                      :class="{ active: currentProgress >= 75 }"
                      class="circle__point-four circle__point">
                </span>
                <div class="circle__background">
                    <PhoneIllustration v-if="isFirstDescription" />
                    <SecondIllustration v-if="isSecondDescription" />
                    <ThirdIllustration v-if="isThirdDescription" />
                </div>
                <DesktopCircle
                    v-if="outerWidth >= 812"
                    @progress="progress"
                    :activateAnimation="activateAnimation"
                    :progressValue="progressValue"
                    :isDuration="isDuration"
                    :fill="fill"
                    :currentProgress="currentProgress"
                    />
                <MobileCircle
                    v-if="outerWidth <= 812"
                    @progress="progress"
                    :activateAnimation="activateAnimation"
                    :progressValue="progressValue"
                    :isDuration="isDuration"
                    :fill="fill"
                    :currentProgress="currentProgress"
                />
            </div>
            <h1 v-if="circleWidth === 250" class="options-container__heading title">How it works</h1>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
import DesktopCircle from './Circles/CircleDesktop'
import MobileCircle from './Circles/CircleMobile'
import PhoneIllustration from './illustration/PhoneIllustration.vue'
import SecondIllustration from './illustration/SecondIllustration.vue'
import ThirdIllustration from './illustration/ThirdIllustration.vue'

export default {
  name: 'SecondScroll',
  components: {
    PhoneIllustration,
    SecondIllustration,
    ThirdIllustration,
    DesktopCircle,
    MobileCircle
  },
  data () {
    return {
      fill: { gradient: ['#9b70fa', '#590ff2'] },
      durationValue: 10000,
      progressValue: 75,
      currentProgress: 0,
      scrolled: 0,
      activateAnimation: false,
      firstActive: false,
      secondActive: false,
      thirdActive: false,
      firstCircle: true,
      secondCircle: false,
      outerWidth: 0,
      circleWidth: 400,
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll)
    window.addEventListener('resize', this.handleResize)
    this.outerWidth = window.innerWidth
    if (window.outerWidth < 500) {
        this.circleWidth = 250
    }

  },
  computed: {
    isFirstDescription() {
      return this.currentProgress >= 0 && this.currentProgress < 26
    },
    isSecondDescription() {
      return this.currentProgress > 26 && this.currentProgress < 51
    },
    isThirdDescription() {
      return this.currentProgress > 51 && this.currentProgress < 76
    },
    isDuration() {
     return { duration: this.durationValue, easing: "linear" }
    },
  },
  methods: {
    updateProgress(value, number) {
      this.progressValue = value
      this.$refs.circle.updateProgress(value)
      switch (number) {
        case 1:
          this.firstActive = true
          this.secondActive = false
          this.thirdActive = false
          break
        case 2:
          this.firstActive = false
          this.secondActive = true
          this.thirdActive = false
          break
        case 3:
          this.firstActive = false
          this.secondActive = false
          this.thirdActive = true
          break
      }
    },
    progress (event, progress, stepValue) {
      this.currentProgress = stepValue
    },
    handleScroll() {
      this.scrolled = Math.floor(window.pageYOffset)
    },
    handleResize() {
      this.outerWidth = Math.floor(window.innerWidth)
    },
  },
  watch: {
    'outerWidth'(value) {
        if (value <= 812) {
            return this.circleWidth = 250
        }
        this.circleWidth = 400
    },
    'scrolled'(value) {
      if (value > 100) {
        this.scrolled = 0
        this.activateAnimation = true
        return window.removeEventListener('scroll', this.handleScroll)
      }
    },
  },
}
</script>

<style scoped lang="scss">
    .second-scroll {
        padding: 0 20px;
        box-sizing: border-box;
    }
    .options-container {
        width: 40%;
        &__heading {
            margin-bottom: 30px;
            color: #292a4b;
        }
    }
    .layout-second-scroll {
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 80px 0;
    }
    .second-scroll {
        background-color: #f3f7fb;
    }

    .options {
        &__wrapper {
            display: flex;
            align-items: center;
            padding: 20px 0 0 0;
        }
        &__icon {
            width: 30px;
            height: 30px;
            padding: 0 20px 0 0;
            opacity: .4;
        }
        &__name {
            margin: 0;
            color: #cad4da;
            font-size: 20px;
            font-weight: 900;
            padding: 0 0 5px 0;
        }
        &__text {
            margin: 0;
            padding: 2px 0 10px 0;
            color: #6a8095;
            font-size: 20px;
            font-weight: 300;
        }
        &__descr {
            padding: 0 0 0 10px;
            line-height: 24px;

        }

    }
    .circle {
        position: relative;
        &__background {
            width: 400px;
            height: 400px;
            position: absolute;
            &:after {
                content: "";
                position: absolute;
                width: 98.4%;
                height: 98.4%;
                border: 3px dashed #a7c1cc;
                border-radius: 50%;
                top: 0;
                left: 0;
            }
        }
        &__point {
            width: 20px;
            height: 20px;
            border: 3px solid #a7c1cc;
            background-color: #f4f7fc;
            border-radius: 50%;
            position: absolute;
            z-index: 3;
        }
        &__point-one {
            right: -11px;
            top: 47%;
        }
        &__point-two {
            right: calc(50% - 10px);
            bottom: -8px;
        }
        &__point-three {
            top: calc(50% - 10px);
            left: -11px;
        }

        &__point-four {
            left: calc(50% - 16px);
            top: -12px;
        }
        .active {
            border: 2px solid #590ff2;
            background-color: #590ff2;
        }
    }
    .icon-active {
        opacity: 1 !important;
    }
    .active-description {
        align-items: end;
        color: #292a4b;
    }
    @media (max-width: 768px), (max-height: 420px){
        .options-container {
            width: 90%;
            padding: 20px 0 40px;
        }
        .layout-second-scroll {
            padding: 0;
        }
        .options-container__heading {
            font-size: 32px;
        }
        .layout-second-scroll {
            flex-direction: column-reverse;
        }
        .circle {
            position: relative;

            &__background {
                width: 250px;
                height: 250px;

                &:after {
                    content: "";
                    width: 244px;
                    height: 243.5px;
                }
            }
            &__point {
                width: 10px;
                height: 10px;
            }
            &__point-one {
                right: -5px;
                top: 46%;
            }
            &__point-two {
                right: calc(50% - 10px);
                bottom: -2px;
            }
            &__point-three {
                top: calc(50% - 10px);
                left: -6px;
            }

            &__point-four {
                left: calc(50% - 8px);
                top: -6px;
            }
        }
        .icon {
            width: 30px;
        }
        .options__name {
            font-size: 18px;
        }
        .options__text {
            font-size: 14px;
        }
        .layout {
            max-width: 320px;
        }
        .second-scroll {
            padding: 0;
        }
    }
</style>
