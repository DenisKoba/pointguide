<template>
    <div class="wrapper fifth-scroll">
        <div class="layout background-fifth-scroll">
            <div class="background-press"></div>
            <div class="press">
                <div class="press-wrapper">
                    <h1 class="press__title title">We`re in press</h1>
                    <div class="press__publication" v-for="release in pressReleases" :class="{ active: release.slideNumber === currentSlide }">
                        <img src="assets/img/press-logo.png" />
                        <h3 class="press__descr-title descr">{{ release.publicationName }}</h3>
                        <h3 class="press__descr descr">{{ release.text }}</h3>
                    </div>
                </div>
            </div>
            <div class="press-navigation">
                <div class="press-navigation__current">
                    <span class="press-navigation__current-slide">{{ currentSlide }}</span>
                    <div class="press-navigation__nav-buttons">
                        <span @click="previousSlide" class="press-navigation__left">
                            <svg width="37" height="37" viewBox="0 0 37 37" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M18.2 36.4C28.2516 36.4 36.4 28.2516 36.4 18.2C36.4 8.14841 28.2516 0 18.2 0C8.14842 0 0 8.14841 0 18.2C0 28.2516 8.14842 36.4 18.2 36.4Z" fill="#E8EFFB"/>
                                <path d="M12.3 18.2C12.3 17.9 12.4 17.6 12.7 17.3L20.2 9.79999C20.7 9.29999 21.5 9.29999 21.9 9.79999C22.4 10.3 22.4 11.1 21.9 11.5L15.3 18.1L21.9 24.7C22.4 25.2 22.4 26 21.9 26.4C21.4 26.9 20.6 26.9 20.2 26.4L12.7 18.9C12.4 18.9 12.3 18.5 12.3 18.2Z" fill="#8230FA"/>
                            </svg>
                        </span>
                        <span @click="nextSlide" class="press-navigation__right">
                            <svg width="40" height="40" viewBox="0 0 40 40" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path d="M37.8985 21.4208C38.8085 11.4105 31.4312 2.55775 21.4208 1.64773C11.4105 0.737712 2.55775 8.115 1.64773 18.1254C0.737714 28.1357 8.115 36.9885 18.1254 37.8985C28.1357 38.8085 36.9885 31.4312 37.8985 21.4208Z" fill="#E8EFFB"/>
                                <path d="M25.3632 20.6687L17.8632 28.1687C17.3632 28.6687 16.5631 28.6687 16.1631 28.1687C15.6631 27.6687 15.6631 26.8687 16.1631 26.4687L22.7631 19.8687L16.1631 13.2687C15.6631 12.7687 15.6631 11.9687 16.1631 11.5687C16.6631 11.0687 17.4632 11.0687 17.8632 11.5687L25.3632 19.0687C25.5632 19.2687 25.7631 19.6687 25.7631 19.9687C25.7631 20.0687 25.6632 20.4687 25.3632 20.6687Z" fill="#8230FA"/>
                            </svg>
                        </span>
                    </div>
                </div>
                <div class="press-navigation__all-pages">
                    <span v-for="slide in slides" class="press-navigation__slides">{{ slide }}</span>
                </div>
            </div>
            <div class="quote">
                <div class="quote-reviews">
                    <img src="../assets/img/coma.png">
                    <div v-for="quote in quotes"
                         class="quote__review"
                         :class="{ active: quote.slideNumber === currentSlide }">
                        <h3 class="quote__review-text">
                            {{ quote.text }}
                        </h3>
                        <div class="quote__author">
                            <div class="quote__name-wrapper">
                                <h3 class="quote__name">{{ quote.name }}</h3>
                                <p class="quote__position">{{ quote.position }}t</p>
                            </div>
                        </div>
                        <a class="read-more-button-link" href="#">
                            <div class="read-more-button">
                                <svg width="29" height="28" viewBox="0 0 29 28" fill="none" xmlns="http://www.w3.org/2000/svg">
                                    <path d="M26.6 14.5L26.9 14.1L26.6 13.7C26.6 13.6 25.5 11.9 23.4 10.2C20.7 7.9 17.5 6.7 14.1 6.7C10.7 6.7 7.49999 7.9 4.79999 10.2C2.69999 11.9 1.69999 13.6 1.59999 13.7L1.29999 14.1L1.59999 14.5C1.59999 14.6 2.69999 16.3 4.79999 18C7.49999 20.3 10.8 21.5 14.1 21.5C17.5 21.5 20.7 20.3 23.4 18C25.5 16.2 26.5 14.5 26.6 14.5ZM22.3 16.7C19.8 18.7 17.1 19.8 14.1 19.8C11.1 19.8 8.29999 18.8 5.89999 16.7C4.59999 15.7 3.79999 14.6 3.29999 14C3.69999 13.4 4.59999 12.4 5.89999 11.3C8.39999 9.3 11.1 8.2 14.1 8.2C17.1 8.2 19.8 9.2 22.3 11.3C23.6 12.4 24.4 13.4 24.9 14C24.5 14.6 23.6 15.7 22.3 16.7Z" fill="#8230FA"/>
                                    <path d="M14.1 9.10001C11.4 9.10001 9.2 11.3 9.2 14C9.2 16.7 11.4 18.9 14.1 18.9C16.8 18.9 19 16.7 19 14C19 11.3 16.8 9.10001 14.1 9.10001ZM14.1 17.3C12.3 17.3 10.8 15.8 10.8 14C10.8 12.2 12.3 10.7 14.1 10.7C15.9 10.7 17.4 12.2 17.4 14C17.4 15.8 15.9 17.3 14.1 17.3Z" fill="#8230FA"/>
                                    <path d="M1.7 1.7H5.1V0H0V5H1.6L1.7 1.7Z" fill="#8230FA"/>
                                    <path d="M23 0V1.60001H26.4V5H28V0H23Z" fill="#8230FA"/>
                                    <path d="M1.7 23H0.100006V28H5.2V26.4H1.8L1.7 23Z" fill="#8230FA"/>
                                    <path d="M26.5 26.4H23.1V28H28.2V23H26.6V26.4H26.5Z" fill="#8230FA"/>
                                </svg>
                                <span>Read more</span>
                            </div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
/* eslint-disable */
  export default {
    name: "FifthScroll",
    data() {
      return {
        slides: [1, 2, 3],
        pressReleases: [
          {
            slideNumber: 1,
            logo: './assets/img/press-logo.png',
            publicationName: 'Esquire',
            text: 'Esquire is a monthly men\'s magazine founded in 1932 in the USA, where it is published by Hearst Corporation. '
          },
          {
            slideNumber: 2,
            logo: './assets/img/press-logo.png',
            publicationName: 'Esquire 2',
            text: 'Esquire is a monthly men\'s magazine founded in 1932 in the USA, where it is published by Hearst Corporation. '
          },
          {
            slideNumber: 3,
            logo: './assets/img/press-logo.png',
            publicationName: 'Esquire 3' ,
            text: 'Esquire is a monthly men\'s magazine founded in 1932 in the USA, where it is published by Hearst Corporation. '
          }
        ],
        quotes: [
          {
            slideNumber: 1,
            text: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis',
            name: 'Andrew',
            position: 'Programmer'
          },
          {
            slideNumber: 2,
            text: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis',
            name: 'Max',
            position: 'Tourist'
          },
          {
            slideNumber: 3,
            text: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis',
            name: 'Dan',
            position: 'Teacher'
          },
        ],
        currentSlide: 1,
      }
    },
   methods: {
     previousSlide() {
       if (this.currentSlide === 1)  {
         return this.currentSlide = 1
       }
       return this.currentSlide = this.currentSlide -= 1
     },
     nextSlide() {
       if (this.currentSlide >= 3)  {
         return this.currentSlide = 3
       }
       return this.currentSlide = this.currentSlide += 1
     },
   },
  }
</script>

<style scoped lang="scss">
    @import url('https://fonts.googleapis.com/css?family=Questrial');

    .active {
        display: block !important;
    }

    .read-more-button {
        display: flex;
        align-items: center;
        & > span {
            padding: 0 0 0 10px;
            color: #9b59fb;
        }
    }

    .read-more-button-link {
        color: #9b59fb;
    }

    .press {
        z-index: 2;
        width: 70%;
        &__publication {
            display: none;
        }
        &__descr-title {
            color: #fff;
            font-weight: 600;
        }
        &__descr {
            color: #fff;
            line-height: 28px;
        }
    }

    .background-fifth-scroll {
        display: flex;
        position: relative;
    }
    .quote {
        position: absolute;
        z-index: 3;
        max-width: 500px;
        box-sizing: border-box;
        padding: 50px;
        background-color: #fff;
        top: 40%;
        right: calc(35% - 250px);
        box-shadow: 0px 0px 40px 4px rgba(23, 23, 23, 0.14);
        &__review-text {
            margin: 0;
            line-height: 28px;
        }
        &__review {
            padding: 0 0 0 20px;
            display: none;
        }
        &__name {
            color: #000000;
        }
    }
    .press-wrapper {
        max-width: 400px;
    }
    .press-navigation {
        z-index: 2;
        display: flex;
        flex-direction: column;
        padding: 0 0 0 30px;
        &__slides {
            font-size: 30px;
            color: #636683;
            padding: 0 30px 0 0;
        }
        &__current-slide {
            font-size: 30px;
            color: #824bf7;
            min-width: 70px;
        }
        &__nav-buttons {
            display: flex;
            align-items: center;
        }
        &__current {
            display: flex;
        }
        &__left, &__right {
            cursor: pointer;
            transition: .3s;
            &:hover {
                transition: .3s;
                opacity: .8;
            }
        }
        &__left {
            margin: 0 10px 0 0;
        }
    }
    .background-press {
        height: 100%;
        width: 100%;
        position: absolute;
        top: 0;
        left: -30%;
        background: #9b70fa;
        background: -moz-linear-gradient(top, #9b70fa 0%, #590ff2 100%);
        background: -webkit-linear-gradient(top, #9b70fa 0%,#590ff2 100%);
        background: linear-gradient(to bottom, #9b70fa 0%,#590ff2 100%);
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#9b70fa', endColorstr='#590ff2',GradientType=0 );
        z-index: 1;
    }
    .background-fifth-scroll {
        padding: 80px 0;
    }
    .press__title {
        margin: 30px 0 60px 0;
        color: #fff;
    }
    .quote-reviews {
        display: flex;
        align-items: end;
        color: #636683;
    }
</style>
