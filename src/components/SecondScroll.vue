<template>
    <div id="second-scroll" class="wrapper second-scroll">
        <div class="layout layout-second-scroll">
            <div class="options-container">
                <h1 class="options-container__heading title">How it works</h1>
                <div id="third-scroll" class="options" @click="updateProgress(25, 1)">
                    <div class="options__wrapper">
                        <svg class="options__icon" v-if="isFirstDescription" width="38" height="38" viewBox="0 0 38 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M19.2 37.4C29.2516 37.4 37.4 29.2516 37.4 19.2C37.4 9.14842 29.2516 1 19.2 1C9.14842 1 1 9.14842 1 19.2C1 29.2516 9.14842 37.4 19.2 37.4Z" stroke="#6807F8" stroke-miterlimit="10"/>
                            <path d="M29.2 18.8C29 18.6 24.7 12.7 19.2 12.7C13.7 12.7 9.3 18.5 9.2 18.8C9 19 9 19.4 9.2 19.6C9.4 19.8 13.7 25.7 19.2 25.7C24.7 25.7 29.1 19.9 29.2 19.6C29.4 19.4 29.4 19.1 29.2 18.8ZM19.2 24.4C15.1 24.4 11.6 20.5 10.6 19.3C11.6 18 15.2 14.2 19.2 14.2C23.3 14.2 26.8 18.1 27.8 19.3C26.8 20.5 23.2 24.4 19.2 24.4Z" fill="#6807F8"/>
                            <path d="M19.2 15.2C17 15.2 15.2 17 15.2 19.2C15.2 21.4 17 23.2 19.2 23.2C21.4 23.2 23.2 21.4 23.2 19.2C23.2 17 21.4 15.2 19.2 15.2ZM19.2 21.9C17.7 21.9 16.5 20.7 16.5 19.2C16.5 17.7 17.7 16.5 19.2 16.5C20.7 16.5 21.9 17.7 21.9 19.2C21.9 20.7 20.6 21.9 19.2 21.9Z" fill="#6807F8"/>
                        </svg>
                        <svg class="options__icon" v-else width="38" height="38" viewBox="0 0 38 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M19.2 37.4C29.2516 37.4 37.4 29.2516 37.4 19.2C37.4 9.14842 29.2516 1 19.2 1C9.14842 1 1 9.14842 1 19.2C1 29.2516 9.14842 37.4 19.2 37.4Z" stroke="#8097A1" stroke-miterlimit="10"/>
                            <path d="M29.2 18.8C29 18.6 24.7 12.7 19.2 12.7C13.7 12.7 9.3 18.5 9.2 18.8C9 19 9 19.4 9.2 19.6C9.4 19.8 13.7 25.7 19.2 25.7C24.7 25.7 29.1 19.9 29.2 19.6C29.4 19.4 29.4 19.1 29.2 18.8ZM19.2 24.4C15.1 24.4 11.6 20.5 10.6 19.3C11.6 18 15.2 14.2 19.2 14.2C23.3 14.2 26.8 18.1 27.8 19.3C26.8 20.5 23.2 24.4 19.2 24.4Z" fill="#8097A1"/>
                            <path d="M19.2 15.2C17 15.2 15.2 17 15.2 19.2C15.2 21.4 17 23.2 19.2 23.2C21.4 23.2 23.2 21.4 23.2 19.2C23.2 17 21.4 15.2 19.2 15.2ZM19.2 21.9C17.7 21.9 16.5 20.7 16.5 19.2C16.5 17.7 17.7 16.5 19.2 16.5C20.7 16.5 21.9 17.7 21.9 19.2C21.9 20.7 20.6 21.9 19.2 21.9Z" fill="#8097A1"/>
                        </svg>
                        <div class="options__descr">
                            <h3 class="options__name">How it works</h3>
                            <p v-if="isFirstDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
                <div class="options" @click="updateProgress(50, 2)">
                    <div class="options__wrapper">
                        <svg class="options__icon" v-if="isSecondDescription" width="38" height="38" viewBox="0 0 38 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M19.2 37.4C29.2516 37.4 37.4 29.2516 37.4 19.2C37.4 9.14842 29.2516 1 19.2 1C9.14841 1 1 9.14842 1 19.2C1 29.2516 9.14841 37.4 19.2 37.4Z" stroke="#6807F8" stroke-miterlimit="10"/>
                            <path d="M19.2 8.7C14.6 8.7 10.8 12.5 10.8 17.1C10.8 17.6 10.8 18.2 10.9 18.7C10.9 18.7 10.9 18.8 11 19C11.1 19.6 11.3 20.1 11.6 20.7C12.5 22.8 14.5 26.1 18.9 29.6C19 29.7 19.1 29.7 19.3 29.7C19.4 29.7 19.6 29.7 19.7 29.6C24.1 26.1 26.1 22.8 27 20.7C27.2 20.2 27.4 19.6 27.6 19C27.6 18.8 27.7 18.7 27.7 18.7C27.8 18.2 27.8 17.7 27.8 17.1C27.6 12.5 23.8 8.7 19.2 8.7ZM26.3 18.5C26.3 18.5 26.3 18.6 26.3 18.7C26.2 19.2 26 19.7 25.8 20.1C25 22 23.2 25 19.3 28.2C15.4 25 13.6 22 12.8 20.1C12.6 19.6 12.4 19.2 12.3 18.7C12.3 18.6 12.3 18.5 12.3 18.5C12.2 18 12.2 17.6 12.2 17.1C12.2 13.1 15.4 9.9 19.4 9.9C23.4 9.9 26.6 13.1 26.6 17.1C26.4 17.6 26.4 18 26.3 18.5Z" fill="#6807F8"/>
                            <path d="M19.2 11.9C16.3 11.9 13.9 14.3 13.9 17.2C13.9 20.1 16.3 22.5 19.2 22.5C22.1 22.5 24.5 20.1 24.5 17.2C24.5 14.3 22.1 11.9 19.2 11.9ZM19.2 21.3C16.9 21.3 15.1 19.4 15.1 17.2C15.1 15 17 13.1 19.2 13.1C21.5 13.1 23.3 15 23.3 17.2C23.3 19.4 21.5 21.3 19.2 21.3Z" fill="#6807F8"/>
                        </svg>
                        <svg class="options__icon" v-else width="38" height="38" viewBox="0 0 38 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M19.2 37.4C29.2516 37.4 37.4 29.2516 37.4 19.2C37.4 9.14842 29.2516 1 19.2 1C9.14841 1 1 9.14842 1 19.2C1 29.2516 9.14841 37.4 19.2 37.4Z" stroke="#8097A1" stroke-miterlimit="10"/>
                            <path d="M19.2 8.7C14.6 8.7 10.8 12.5 10.8 17.1C10.8 17.6 10.8 18.2 10.9 18.7C10.9 18.7 10.9 18.8 11 19C11.1 19.6 11.3 20.1 11.6 20.7C12.5 22.8 14.5 26.1 18.9 29.6C19 29.7 19.1 29.7 19.3 29.7C19.4 29.7 19.6 29.7 19.7 29.6C24.1 26.1 26.1 22.8 27 20.7C27.2 20.2 27.4 19.6 27.6 19C27.6 18.8 27.7 18.7 27.7 18.7C27.8 18.2 27.8 17.7 27.8 17.1C27.6 12.5 23.8 8.7 19.2 8.7ZM26.3 18.5C26.3 18.5 26.3 18.6 26.3 18.7C26.2 19.2 26 19.7 25.8 20.1C25 22 23.2 25 19.3 28.2C15.4 25 13.6 22 12.8 20.1C12.6 19.6 12.4 19.2 12.3 18.7C12.3 18.6 12.3 18.5 12.3 18.5C12.2 18 12.2 17.6 12.2 17.1C12.2 13.1 15.4 9.9 19.4 9.9C23.4 9.9 26.6 13.1 26.6 17.1C26.4 17.6 26.4 18 26.3 18.5Z" fill="#8097A1"/>
                            <path d="M19.2 11.9C16.3 11.9 13.9 14.3 13.9 17.2C13.9 20.1 16.3 22.5 19.2 22.5C22.1 22.5 24.5 20.1 24.5 17.2C24.5 14.3 22.1 11.9 19.2 11.9ZM19.2 21.3C16.9 21.3 15.1 19.4 15.1 17.2C15.1 15 17 13.1 19.2 13.1C21.5 13.1 23.3 15 23.3 17.2C23.3 19.4 21.5 21.3 19.2 21.3Z" fill="#8097A1"/>
                        </svg>
                        <div class="options__descr">
                            <h3 class="options__name">Friends</h3>
                            <p v-if="isSecondDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
                <div class="options">
                    <div class="options__wrapper" @click="updateProgress(75, 3)">
                        <svg class="options__icon" v-if="isThirdDescription" width="38" height="38" viewBox="0 0 38 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M23 21.3C22.8 21.2 22.6 21.2 22.4 21.3C21.6 22.2 20.4 22.7 19.2 22.7C18 22.7 16.8 22.2 16 21.3C15.9 21.1 15.6 21.1 15.4 21.3C15.2 21.4 15.2 21.7 15.4 21.9C16.4 23 17.8 23.6 19.2 23.6C20.7 23.6 22 23 23 21.9C23.1 21.7 23.1 21.4 23 21.3Z" fill="#6807F8" stroke="#6807F8" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M19.2 10.2C14.2 10.2 10.2 14.2 10.2 19.2C10.2 24.2 14.2 28.2 19.2 28.2C24.2 28.2 28.2 24.2 28.2 19.2C28.2 14.2 24.1 10.2 19.2 10.2ZM19.2 27.5C14.7 27.5 11 23.8 11 19.3C11 14.8 14.7 11.1 19.2 11.1C23.7 11.1 27.4 14.8 27.4 19.3C27.4 23.8 23.7 27.5 19.2 27.5Z" fill="#6807F8" stroke="#6807F8" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M22.3 16.5C21.2 16.5 20.3 17.4 20.3 18.5C20.3 18.7 20.5 18.9 20.7 18.9C20.9 18.9 21.1 18.7 21.1 18.5C21.1 17.9 21.6 17.3 22.3 17.3C23 17.3 23.5 17.8 23.5 18.5C23.5 18.7 23.7 18.9 23.9 18.9C24.1 18.9 24.3 18.7 24.3 18.5C24.3 17.4 23.4 16.5 22.3 16.5Z" fill="#6807F8" stroke="#6807F8" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M17.2 18.5C17.2 18.7 17.4 18.9 17.6 18.9C17.8 18.9 18 18.7 18 18.5C18 17.4 17.1 16.5 16 16.5C14.9 16.5 14 17.4 14 18.5C14 18.7 14.2 18.9 14.4 18.9C14.6 18.9 14.8 18.7 14.8 18.5C14.8 17.9 15.3 17.3 16 17.3C16.7 17.3 17.2 17.8 17.2 18.5Z" fill="#6807F8" stroke="#6807F8" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M19.2 37.4C29.2516 37.4 37.4 29.2516 37.4 19.2C37.4 9.14842 29.2516 1 19.2 1C9.14842 1 1 9.14842 1 19.2C1 29.2516 9.14842 37.4 19.2 37.4Z" stroke="#6807F8" stroke-miterlimit="10"/>
                        </svg>
                        <svg class="options__icon" v-else width="38" height="38" viewBox="0 0 38 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path d="M23 21.3C22.8 21.2 22.6 21.2 22.4 21.3C21.6 22.2 20.4 22.7 19.2 22.7C18 22.7 16.8 22.2 16 21.3C15.9 21.1 15.6 21.1 15.4 21.3C15.2 21.4 15.2 21.7 15.4 21.9C16.4 23 17.8 23.6 19.2 23.6C20.7 23.6 22 23 23 21.9C23.1 21.7 23.1 21.4 23 21.3Z" fill="#8097A1" stroke="#8097A1" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M19.2 10.2C14.2 10.2 10.2 14.2 10.2 19.2C10.2 24.2 14.2 28.2 19.2 28.2C24.2 28.2 28.2 24.2 28.2 19.2C28.2 14.2 24.1 10.2 19.2 10.2ZM19.2 27.5C14.7 27.5 11 23.8 11 19.3C11 14.8 14.7 11.1 19.2 11.1C23.7 11.1 27.4 14.8 27.4 19.3C27.4 23.8 23.7 27.5 19.2 27.5Z" fill="#8097A1" stroke="#8097A1" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M22.3 16.5C21.2 16.5 20.3 17.4 20.3 18.5C20.3 18.7 20.5 18.9 20.7 18.9C20.9 18.9 21.1 18.7 21.1 18.5C21.1 17.9 21.6 17.3 22.3 17.3C23 17.3 23.5 17.8 23.5 18.5C23.5 18.7 23.7 18.9 23.9 18.9C24.1 18.9 24.3 18.7 24.3 18.5C24.3 17.4 23.4 16.5 22.3 16.5Z" fill="#8097A1" stroke="#8097A1" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M17.2 18.5C17.2 18.7 17.4 18.9 17.6 18.9C17.8 18.9 18 18.7 18 18.5C18 17.4 17.1 16.5 16 16.5C14.9 16.5 14 17.4 14 18.5C14 18.7 14.2 18.9 14.4 18.9C14.6 18.9 14.8 18.7 14.8 18.5C14.8 17.9 15.3 17.3 16 17.3C16.7 17.3 17.2 17.8 17.2 18.5Z" fill="#8097A1" stroke="#8097A1" stroke-width="0.5" stroke-miterlimit="10"/>
                            <path d="M19.2 37.4C29.2516 37.4 37.4 29.2516 37.4 19.2C37.4 9.14842 29.2516 1 19.2 1C9.14842 1 1 9.14842 1 19.2C1 29.2516 9.14842 37.4 19.2 37.4Z" stroke="#8097A1" stroke-miterlimit="10"/>
                        </svg>

                        <div class="options__descr">
                            <h3 class="options__name">Travel</h3>
                            <p v-if="isThirdDescription" class="options__text">Select a city and pick a tour you like. Guide by user scores and reviews</p>
                        </div>
                    </div>
                </div>
            </div>
            <div class="circle">
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
                   <!-- <PhoneIllustration v-if="isFirstDescription" />
                    <SecondIllustration v-if="isSecondDescription" />-->
                    <ThirdIllustration  />
                </div>
                <vue-circle
                        v-if="activateAnimation"
                        :progress="progressValue"
                        :size="400"
                        :reverse="false"
                        line-cap="round"
                        :fill="fill"
                        empty-fill="rgba(0, 0, 0, .1)"
                        :animation-start-value="0.0"
                        :animation="isDuration"
                        :start-angle="0"
                        insert-mode="append"
                        :thickness="2"
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
        }
        &__text {
            margin: 0;
        }

    }
    .circle {
        position: relative;
        &__background {
            width: 400px;
            height: 400px;
            position: absolute;
        }
        &__point {
            width: 20px;
            height: 20px;
            border: 2px solid #dbdee1;
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
            bottom: -4px;
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
</style>
