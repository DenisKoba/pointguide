<template>
    <div class="wrapper fourth-scroll">
        <div class="layout layout-fourth-scroll">
            <h1 class="title fourth-scroll-title">Customer Reviews</h1>
            <carousel navigationNextLabel=""
                      navigationPrevLabel=""
                      :navigationEnabled="true"
                      :loop="true"
                      :autoplayTimeout="5000"
                      :perPageCustom="perPageCount"
                      >
                <slide>
                    <div class="customer-reviews">
                        <div class="customer-reviews__review">
                            <img class="customer-reviews__coma" src="../assets/img/coma.png">
                            <h3 class="customer-reviews__review-text">
                                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
                            </h3>
                        </div>
                        <div class="customer-reviews__author">
                            <img src="../assets/img/author-photo.png"/>
                            <div class="customer-reviews__name-wrapper">
                                <h3 class="customer-reviews__name">Name</h3>
                                <p class="customer-reviews__position">Tourist</p>
                            </div>
                        </div>
                    </div>
                </slide>
                <slide>
                    <div class="customer-reviews">
                        <div class="customer-reviews__review">
                            <img class="customer-reviews__coma" src="../assets/img/coma.png">
                            <h3 class="customer-reviews__review-text">
                                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
                            </h3>
                        </div>
                        <div class="customer-reviews__author">
                            <img src="../assets/img/author-photo.png"/>
                            <div class="customer-reviews__name-wrapper">
                                <h3 class="customer-reviews__name">Name</h3>
                                <p class="customer-reviews__position">Tourist</p>
                            </div>
                        </div>
                    </div>
                </slide>
                <slide>
                    <div class="customer-reviews">
                        <div class="customer-reviews__review">
                            <img class="customer-reviews__coma" src="../assets/img/coma.png">
                            <h3 class="customer-reviews__review-text">
                                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
                            </h3>
                        </div>
                        <div class="customer-reviews__author">
                            <img src="../assets/img/author-photo.png"/>
                            <div class="customer-reviews__name-wrapper">
                                <h3 class="customer-reviews__name">Name</h3>
                                <p class="customer-reviews__position">Tourist</p>
                            </div>
                        </div>
                    </div>
                </slide>
                <slide>
                    <div class="customer-reviews">
                        <div class="customer-reviews__review">
                            <img class="customer-reviews__coma" src="../assets/img/coma.png">
                            <h3 class="customer-reviews__review-text">
                                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
                            </h3>
                        </div>
                        <div class="customer-reviews__author">
                            <img src="../assets/img/author-photo.png"/>
                            <div class="customer-reviews__name-wrapper">
                                <h3 class="customer-reviews__name">Name</h3>
                                <p class="customer-reviews__position">Tourist</p>
                            </div>
                        </div>
                    </div>
                </slide>
                <slide>
                    <div class="customer-reviews">
                        <div class="customer-reviews__review">
                            <img class="customer-reviews__coma" src="../assets/img/coma.png">
                            <h3 class="customer-reviews__review-text">
                                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
                            </h3>
                        </div>
                        <div class="customer-reviews__author">
                            <img src="../assets/img/author-photo.png"/>
                            <div class="customer-reviews__name-wrapper">
                                <h3 class="customer-reviews__name">Name</h3>
                                <p class="customer-reviews__position">Tourist</p>
                            </div>
                        </div>
                    </div>
                </slide>
                <slide>
                    <div class="customer-reviews">
                        <div class="customer-reviews__review">
                            <img class="customer-reviews__coma" src="../assets/img/coma.png">
                            <h3 class="customer-reviews__review-text">
                                Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
                            </h3>
                        </div>
                        <div class="customer-reviews__author">
                            <img src="../assets/img/author-photo.png"/>
                            <div class="customer-reviews__name-wrapper">
                                <h3 class="customer-reviews__name">Name</h3>
                                <p class="customer-reviews__position">Tourist</p>
                            </div>
                        </div>
                    </div>
                </slide>
            </carousel>
        </div>
    </div>
</template>

<script>
  /* eslint-disable */
  import { Carousel, Slide } from 'vue-carousel'
  export default {
    name: "FourthScroll",
    components: {
      Carousel,
      Slide,
    },
      data() {
        return {
            perPageCount: [[320, 1], [769, 2]],
        }
      }
  }
</script>

<style scoped lang="scss">
    @import url('https://fonts.googleapis.com/css?family=Questrial');
    .fourth-scroll-title {
        text-align: center;
        color: #292a4b;
    }
    .fourth-scroll {
        background-color: #f3f7fb;
        padding: 30px 0 60px;
        box-sizing: border-box;
    }
    .customer-reviews {
        align-items: center;
        justify-content: center;
        display: flex;
        flex-direction: column;
        &__review {
            display: -webkit-box;
            display: -ms-flexbox;
            display: flex;
            -webkit-box-align: end;
            -ms-flex-align: end;
            align-items: end;
            padding: 40px;
            max-width: 490px;
            -webkit-box-sizing: border-box;
            box-sizing: border-box;
            background-color: #e8effb;
            position: relative;
            &:after {
                content: '';
                width: 0;
                height: 0;
                border-style: solid;
                border-width: 35px 0px 0 30px;
                border-color: #e8effb transparent transparent transparent;
                position: absolute;
                bottom: -34px;
            }
        }
        &__coma {
            margin: 20px 20px 0 0;
        }
        &__review-text {
            font-family: "Questrial", sans-serif;
            color: #636683;
            font-weight: 300;
            line-height: 26px;
        }
        &__author {
            display: flex;
            justify-content: center;
            align-items: end;
            margin: 50px 0 0 0;
            & > img {
                padding: 0 10px 0 0;
            }
        }
        &__name {
            padding: 0 0 5px 0;
        }
        &__position {
            color: #8ea0b0;
        }
        &__name, &__position {
            margin: 0;
        }
        &__name-wrapper {
            padding: 10px 0 0 0;
        }
    }

    .layout-fourth-scroll {
        padding: 30px 0;
    }
    @media (max-width: 768px), (max-height: 420px){
        .title {
            font-size: 25px;
            line-height: 30px;
            margin: 0;
        }
        .layout {
            padding: 0;
        }
        .customer-reviews__review {
            padding: 5px 20px;
            font-weight: 600;
            font-size: 12px;
            line-height: 14px;
            max-width: 66%;
            box-sizing: border-box;
            &-text {
                line-height: 18px;
                font-weight: 400;
            }
            .customer-reviews__coma {
                width: 19px;
            }
        }
        .customer-reviews__author {
           & > img {
               width: 40px;
               height: 40px;
           }
        }
        .customer-reviews__name {
            font-size: 11px;
        }
        .customer-reviews__position {
            font-size: 10px;
        }
        .customer-reviews__author {
            margin: 31px 0 0 0;
        }
    }

</style>
