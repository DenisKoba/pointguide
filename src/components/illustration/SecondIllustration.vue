<template>
    <div class="second-illustration">
        <img class="second-illustration__part second-illustration__plants" src="../../assets/img/second-illustration/plants.svg">
        <img class="second-illustration__part second-illustration__sights" src="../../assets/img/second-illustration/background.svg">
        <img class="second-illustration__part second-illustration__guy" src="../../assets/img/second-illustration/guy.svg">
    </div>
</template>

<script>
  export default {
    name: "SecondIllustration"
  }
</script>

<style scoped lang="scss">
    .second-illustration {
        animation: animate-illustration .3s ease forwards;
        position: absolute;
        top: 20px;
        left: 20px;
        width: 90%;
        height: 90%;
        border-radius: 50%;
        overflow: hidden;
        background-color: #fff
    }

    .second-illustration__part {
        position: absolute
    }

    .second-illustration__plants {
        top: 55%;
        right: calc(50% - 150px);
        width: 300px;
        z-index: 1;
        animation: animate-plants 1s ease forwards
    }

    .second-illustration__guy {
        width: 180px;
        left: calc(50% - 85px);
        top: 78px;
        animation: animate-guy 1.5s ease forwards;
        z-index: 2
    }

    .second-illustration__sights{
        width: 230px;
        top: 42px;
        left: calc(50% - 134px);
        animation: animate-background 2s ease forwards
    }

    @keyframes animate-plants {
        0% {
            right: 50%;
            opacity: 0
        }
        to {
            right: calc(50% - 150px);
            opacity: 1
        }
    }

    @keyframes animate-guy {
        0% {
            left: -100px;
            opacity: 0
        }
        to {
            left: calc(50% - 85px);
            opacity: 1
        }
    }

    @keyframes animate-background {
        0% {
            left: -100px;
            opacity: 0
        }
        to {
            left: calc(50% - 134px);
            opacity: 1
        }
    }

    @keyframes animate-illustration {
        0% {
            opacity: 0
        }
        to {
            opacity: 1
        }
    }
    @media (max-width: 768px), (max-height: 420px) {
        .second-illustration {
            top: 13px;
            left: 13px;
        }
        .second-illustration__plants {
            top: 55%;
            left: 20px;
            width: 180px;
            z-index: 1;
            animation: animate-plants 1s ease forwards
        }

        .second-illustration__guy {
            width: 106px;
            top: 45px;
            animation: animate-guy 1.5s ease forwards;
            z-index: 2
        }

        .second-illustration__sights{
            width: 124px;
            top: 42px;
            left: 120px;
            animation: animate-background 2s ease forwards
        }

        @keyframes animate-plants {
            0% {
                left: 0;
                opacity: 0
            }
            100% {
                left: 20px;
                opacity: 1
            }
        }

        @keyframes animate-guy {
            0% {
                left: -10px;
                opacity: 0
            }
            to {
                left: 90px;
                opacity: 1
            }
        }

        @keyframes animate-background {
            0% {
                left: -100px;
                opacity: 0
            }
            to {
                left: 20px;
                opacity: 1
            }
        }

        @keyframes animate-illustration {
            0% {
                opacity: 0
            }
            to {
                opacity: 1
            }
        }
    }
</style>
