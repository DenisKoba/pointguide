<template>
    <div class="third-illustration">
        <img class="third-illustration__part third-illustration__grass" src="../../assets/img/third-illustration/grass.svg">
        <img class="third-illustration__part third-illustration__man" src="../../assets/img/third-illustration/man.svg">
        <img class="third-illustration__part third-illustration__point" src="../../assets/img/third-illustration/point.svg">
    </div>
</template>

<script>
  export default {
    name: "ThirdIllustration"
  }
</script>

<style scoped lang="scss">
    .third-illustration {
        animation: animate-illustration-data-v-64e7e06c .3s ease forwards;
        position: absolute;
        top: 20px;
        left: 20px;
        width: 90%;
        height: 90%;
        border-radius: 50%;
        overflow: hidden;
        background-color: #fff
    }

    .third-illustration__part {
        position: absolute
    }

    .third-illustration__grass {
        top: 55%;
        right: calc(50% - 150px);
        width: 300px;
        z-index: 1;
        animation: animate-plants 2s ease forwards
    }

    .third-illustration__man {
        width: 214px;
        left: calc(50% - 85px);
        top: 78px;
        animation: animate-guy 1s ease forwards;
        z-index: 3
    }

    .third-illustration__point {
        width: 215px;
        top: 65px;
        left: calc(50% - 165px);
        animation: animate-background 1.5s ease forwards;
        z-index: 2
    }

    @keyframes animate-plants {
        0% {
            opacity: 0
        }
        to {
            opacity: 1
        }
    }

    @keyframes animate-guy {
        0% {
            opacity: 0
        }
        to {
            opacity: 1
        }
    }

    @keyframes animate-background {
        0% {
            opacity: 0
        }
        60% {
            opacity: 0
        }
        to {
            opacity: 1
        }
    }

    @keyframes animate-illustration-data-v-64e7e06c {
        0% {
            opacity: 0
        }
        to {
            opacity: 1
        }
    }
</style>
