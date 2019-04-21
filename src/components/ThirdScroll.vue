<template>
    <div id="third-scroll" class="wrapper third-section">
        <div class="layout">
            <div class="download__mobile">
                <div :class="{ 'active-first': scrolledEnougth }" class="download__mobile_first download__mobile_phone"></div>
                <div :class="{ 'active-second': scrolledEnougth }" class="download__mobile_second download__mobile_phone"></div>
            </div>
            <div class="download__descr">
               <h2 class="download__heading ">Download</h2>
                <svg width="422" height="49" viewBox="0 0 422 49" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M15.1027 33.3305V41.2663C15.1027 45.2342 12.3252 47.615 7.96049 47.615C3.19899 47.615 0.818237 44.8374 0.818237 41.2663V7.93579C0.818237 3.96787 3.59578 1.58713 7.96049 1.58713H21.0546C34.1487 1.58713 41.291 8.72938 41.291 17.4588C41.291 26.1882 34.1487 33.3305 21.0546 33.3305C21.0546 33.3305 15.1027 33.3305 15.1027 33.3305ZM21.0546 21.4267C24.2289 21.4267 26.2129 19.4428 26.2129 17.062C26.2129 14.6812 24.2289 12.6973 21.0546 12.6973H15.1027V21.0299L21.0546 21.4267Z" fill="white"/>
                    <path d="M89.3028 28.569C89.3028 39.6792 80.9702 48.0118 67.4793 48.0118C53.9883 48.0118 45.6557 39.6792 45.6557 28.569V19.4428C45.6557 8.33263 53.9883 0 67.4793 0C80.9702 0 89.3028 8.33263 89.3028 19.4428V28.569ZM74.6215 19.4428C74.6215 14.2845 71.4472 11.1102 67.4793 11.1102C63.5113 11.1102 60.337 14.2845 60.337 19.4428V28.569C60.337 33.7273 63.5113 36.9016 67.4793 36.9016C71.4472 36.9016 74.6215 33.7273 74.6215 28.569V19.4428Z" fill="white"/>
                    <path d="M110.333 40.8695C110.333 44.8374 107.555 47.2182 103.191 47.2182C98.429 47.2182 96.0482 44.4406 96.0482 40.8695V6.74542C96.0482 2.7775 98.8258 0.396759 103.191 0.396759C107.952 0.396759 110.333 3.1743 110.333 6.74542V40.8695Z" fill="white"/>
                    <path d="M133.347 26.1883V41.2663C133.347 45.2343 130.569 47.615 126.204 47.615C121.443 47.615 119.062 44.8375 119.062 41.2663V7.14224C119.062 3.17432 121.84 0.793579 126.204 0.793579C130.172 0.793579 132.553 3.17432 135.331 7.14224L146.441 22.2203H147.234V7.14224C147.234 3.17432 150.012 0.793579 154.377 0.793579C159.138 0.793579 161.519 3.57112 161.519 7.14224V41.2663C161.519 45.2343 158.741 47.615 154.377 47.615C150.409 47.615 148.028 45.2343 145.25 41.2663L134.14 26.1883H133.347V26.1883Z" fill="white"/>
                    <path d="M173.026 14.2845C168.264 14.2845 165.884 11.5069 165.884 7.93579C165.884 3.96787 168.661 1.58713 173.026 1.58713H201.992C206.753 1.58713 209.134 4.36466 209.134 7.93579C209.134 11.9037 206.356 14.2845 201.992 14.2845H194.453V41.2663C194.453 45.2342 191.675 47.615 187.31 47.615C182.549 47.615 180.168 44.8374 180.168 41.2663V14.2845H173.026Z" fill="white"/>
                    <path d="M211.515 19.4428C211.515 8.33263 219.847 0 233.338 0C244.845 0 251.194 6.34867 251.194 11.1102C251.194 14.6813 248.813 17.062 244.052 17.062C238.893 17.062 238.1 12.3006 233.338 12.3006C228.974 12.3006 226.196 15.0781 226.196 19.4428V28.569C226.196 32.9337 228.974 35.7113 233.338 35.7113C236.909 35.7113 239.687 33.7273 239.687 33.7273V30.9498H237.703C233.735 30.9498 231.354 28.1722 231.354 24.9979C231.354 21.8236 234.132 19.046 237.703 19.046H246.829C250.797 19.046 252.781 21.03 252.781 24.9979V36.9016C252.781 41.6631 245.639 48.0118 233.338 48.0118C219.847 48.0118 211.515 39.6792 211.515 28.569V19.4428V19.4428Z" fill="white"/>
                    <path d="M259.526 29.3626V7.14224C259.526 3.17432 262.304 0.793579 266.669 0.793579C271.43 0.793579 273.811 3.57112 273.811 7.14224V29.3626C273.811 34.1241 276.588 36.5048 280.16 36.5048C284.128 36.5048 286.508 33.7273 286.508 29.3626V7.14224C286.508 3.17432 289.286 0.793579 293.651 0.793579C298.412 0.793579 300.793 3.57112 300.793 7.14224V29.3626C300.793 40.4728 292.857 48.4086 279.763 48.4086C267.462 48.4086 259.526 40.4728 259.526 29.3626Z" fill="white"/>
                    <path d="M324.6 40.8695C324.6 44.8374 321.823 47.2182 317.458 47.2182C312.697 47.2182 310.316 44.4406 310.316 40.8695V6.74542C310.316 2.7775 313.093 0.396759 317.458 0.396759C322.22 0.396759 324.6 3.1743 324.6 6.74542V40.8695Z" fill="white"/>
                    <path d="M374.199 27.3786C374.199 38.4888 365.867 46.8214 351.582 46.8214H340.075C335.314 46.8214 332.933 44.0438 332.933 40.4727V7.93579C332.933 3.96787 335.711 1.58713 340.075 1.58713H351.582C365.47 1.58713 374.199 9.91975 374.199 21.0299V27.3786ZM347.217 13.0941V35.3144H351.582C356.344 35.3144 359.518 32.1401 359.518 27.3786V21.0299C359.518 16.2684 356.344 13.0941 351.582 13.0941H347.217Z" fill="white"/>
                    <path d="M395.626 14.2845V18.2524H407.927C411.895 18.2524 414.275 21.0299 414.275 24.2043C414.275 27.3786 411.498 30.1561 407.927 30.1561H395.626V34.1241H413.878C418.64 34.1241 421.021 36.9016 421.021 40.4727C421.021 44.0438 418.243 46.8214 413.878 46.8214H388.484C383.722 46.8214 381.342 44.0438 381.342 40.4727V7.93579C381.342 3.96787 384.119 1.58713 388.484 1.58713H413.482C418.243 1.58713 420.624 4.36466 420.624 7.93579C420.624 11.9037 417.846 14.2845 413.482 14.2845H395.626Z" fill="white"/>
                </svg>

                <h3 class="download__text descr">Enjoy high quality audio tours from different authors and styles. Сustomize
                    your experience and have fun traveling</h3>
                <DownloadButtons />
            </div>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
  import DownloadButtons from './DownloadButtons'

  export default {
    name: "ThirdScroll",
    components: {
      DownloadButtons,
    },
    data() {
      return {
        scrolled: 0,
        scrolledEnougth: false,
      }
    },
    created () {
      window.addEventListener('scroll', this.handleScroll)
    },
    methods: {
      handleScroll() {
        this.scrolled = Math.floor(window.pageYOffset)
      },
    },
    watch: {
      'scrolled'(value) {
        if (value > document.getElementById('second-scroll').offsetTop) {
          this.scrolledEnougth = true
        }
        if (value > document.getElementById('third-scroll')) {
          window.removeEventListener('scroll', this.handleScroll)
        }
      }
    },
  }
</script>

<style scoped lang="scss">
    @font-face {
        font-family: "Acrom Regular";
        src: url('../fonts/Acrom-Regular.ttf');
    }
    .third-section {
        background: #9b70fa;
        background: -moz-linear-gradient(top, #9b70fa 0%, #590ff2 100%);
        background: -webkit-linear-gradient(top, #9b70fa 0%,#590ff2 100%);
        background: linear-gradient(to bottom, #9b70fa 0%,#590ff2 100%);
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#9b70fa', endColorstr='#590ff2',GradientType=0 );
        padding: 100px 0;
        overflow: hidden;
    }
    .layout {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .download {
        &__mobile {
            width: 50%;
            &_phone {
                width: 380px;
                height: 550px;
                position: absolute;
                left: -40px;
                background-repeat: no-repeat;
                background-position: top center;
                background-size: cover;
            }
            &_first {
                background-image: url("../assets/img/phone1.png");
                top: 50px;
                z-index: 2;
                transition: .8s;
            }
            &_second {
                background-image: url("../assets/img/phone2.png");
                left: 150px;
                top: 100px;
                z-index: 1;
                transition: 1s;
            }
         }
        &__descr {
            width: 40%;
        }
        &__text {
            color: #fff;
            font-size: 22px;
        }
        &__heading {
            color: #fff;
            font-size: 30px;
            font-family: "Acrom Regular", sans-serif;
        }
    }
    .active-first {
        top: -50px;
        transition: .8s;
    }
    .active-second {
        top: -10px;
        transition: 1.5s;
    }
</style>
