<template>
    <div class="wrapper fourth-scroll">
        <div class="layout layout-fourth-scroll">
            <h1 class="title fourth-scroll-title">Customer Reviews</h1>
            <carousel navigationNextLabel=""
                      navigationPrevLabel=""
                      :navigationEnabled="true"
                      :loop="true"
                      :autoplayTimeout="5000"
                      :autoplay="true">
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
  }
</script>

<style scoped lang="scss">
    @font-face {
        font-family: "Acrom Regular";
        src: url('../fonts/Acrom-Regular.ttf');
    }
    @font-face {
        font-family: "Circe Regular";
        src: url('../fonts/Circe-Regular.ttf');
    }
    .fourth-scroll-title {
        text-align: center;
        color: #292a4b;
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
            font-family: "Circe", sans-serif;
            color: #636683;
            font-weight: 300;
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
        &__name, &__position {
            margin: 0;
            color: #292a4b;
        }
        &__name-wrapper {
            padding: 10px 0 0 0;
        }
    }

    .layout-fourth-scroll {
        padding: 30px 0;
    }

</style>
