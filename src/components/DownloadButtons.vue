<template>
    <div class="container">
        <div class="container__app-store container__button">
            <a href="#">
                <img class="button" src="../assets/img/apple-button.svg">
            </a>
        </div>
        <div class="container__google-play container__button">
            <a href="#">
                <img class="button" src="../assets/img/google-button.svg" />
            </a>
        </div>
    </div>
</template>

<script>
  /* eslint-disable */
export default {
  name: 'DownloadButtons'
}
</script>

<style scoped lang="scss">
    .container {
        display: flex;
        -ms-flex-align: center;
        align-items: center;
        margin: 50px 0 0 0;
        max-width: 420px;
        justify-content: end;
        &__google-play, &__app-store {
            cursor: pointer;
            transition: .3s;
            &:hover {
                transition: .3s;
                opacity: .9;
            }
        }
        &__google-play {
            padding: 0 0 0 20px;
        }
        &__apple-pay {
            padding: 0 20px 0 0;
        }
    }
    @media (max-width: 500px), (max-height: 420px){
        .button {
            height: 40px;
        }
        .container {
            margin: 20px 0 0 0;
        }
    }
</style>
