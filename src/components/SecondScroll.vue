<template>
    <div id="second-scroll" class="wrapper second-scroll">
        <div class="layout layout-second-scroll">
            <div class="options-container">
                <h1 class="options-container__heading title">How it works</h1>
                <div id="third-scroll" class="options" @click="updateProgress(25, 1)">
                    <div :class="{ 'active-description': isFirstDescription }" class="options__wrapper">
                        <img v-if="isFirstDescription" src="../assets/img/eye-icon-active.svg" />
                        <img v-else src="../assets/img/eye-icon.svg" />
                        <div class="options__descr">
                            <h3 :class="{ 'active-description': isFirstDescription }" class="options__name">How it works</h3>
                            <p v-if="isFirstDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
                <div class="options" @click="updateProgress(50, 2)">
                    <div :class="{ 'active-description': isSecondDescription }" class="options__wrapper">
                        <img v-if="isSecondDescription" src="../assets/img/point-icon-active.svg" />
                        <img v-else src="../assets/img/point-icon.svg" />
                        <div class="options__descr">
                            <h3 :class="{ 'active-description': isSecondDescription }" class="options__name">Friends</h3>
                            <p v-if="isSecondDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
                <div class="options" @click="updateProgress(75, 3)">
                    <div :class="{ 'active-description': isThirdDescription }" class="options__wrapper">
                        <img src="../assets/img/smile-icon-active.svg" v-if="isThirdDescription" />
                        <img src="../assets/img/smile-icon.svg" v-else />
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
                    <PhoneIllustration  />
                    <!--<SecondIllustration v-if="isSecondDescription" />
                    <ThirdIllustration v-if="isThirdDescription" />-->
                </div>
                <vue-circle
                        v-if="activateAnimation"
                        :progress="progressValue"
                        :size="400"
                        :reverse="false"
                        line-cap="round"
                        :fill="fill"
                        empty-fill="rgba(251, 251, 251, 0)"
                        :animation-start-value="0.0"
                        :animation="isDuration"
                        :start-angle="0"
                        insert-mode="append"
                        :thickness="3"
                        ref="circle"
                        @vue-circle-progress="progress">
                </vue-circle>
            </div>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
import VueCircle from 'vue2-circle-progress'
import PhoneIllustration from './illustration/PhoneIllustration.vue'
import SecondIllustration from './illustration/SecondIllustration.vue'
import ThirdIllustration from './illustration/ThirdIllustration.vue'

export default {
  name: 'SecondScroll',
  components: {
    VueCircle,
    PhoneIllustration,
    SecondIllustration,
    ThirdIllustration
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
    }
  },
  created () {
    window.addEventListener('scroll', this.handleScroll);
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
  },
  watch: {
    'scrolled'(value) {
      if (value > 100) {
        this.scrolled = 0
        this.activateAnimation = true
        return window.removeEventListener('scroll', this.handleScroll)
      }
    },
    'currentProgress'(value) {
      if(value === 75) {
        setTimeout(() => {
          this.$refs.circle.updateProgress(0)
        }, 2000)
      }
      if (value === 0) {
        setTimeout(() => {
          this.$refs.circle.updateProgress(75)
        }, 2000)
      }
    }
  },
}
</script>

<style scoped lang="scss">
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
    @media (max-width: 500px), (max-height: 420px){
        .layout-second-scroll {
            flex-direction: column-reverse;
        }
    }
</style>
