<template>
    <div class="phone-illustration">
        <img class="phone-illustration__part phone-illustration__pocket" src="../../assets/img/phone-illustration/pocket.svg">
        <img class="phone-illustration__part phone-illustration__background" src="../../assets/img/phone-illustration/phone-animation-background.png">
        <div class="phone-illustration__phone">
            <img class="phone-illustration__part phone-illustration__eyes" src="../../assets/img/phone-illustration/eyes.svg">
            <img class="phone-illustration__part phone-illustration__mouth" src="../../assets/img/phone-illustration/mouth.svg">
            <img class="phone-illustration__part phone-illustration__phone" src="../../assets/img/phone-illustration/phone-for-animation.svg">
        </div>
    </div>
</template>

<script>
  export default {
    name: "PhoneIllustration"
  }
</script>

<style scoped lang="scss">
    .phone-illustration {
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

    .phone-illustration__part {
        position: absolute
    }

    .phone-illustration__pocket {
        top: 200px;
        right: calc(50% - 110px);
        width: 220px;
        z-index: 2
    }

    .phone-illustration__phone {
        width: 170px;
        left: calc(50% - 85px);
        top: 78px;
        animation: animate-phone 1.5s ease forwards
    }

    .phone-illustration__background {
        width: 290px;
        top: 42px;
        left: calc(50% - 134px);
        animation: animate-background 2s ease forwards
    }

    .phone-illustration__eyes {
        width: 70px;
        top: 135px;
        left: calc(50% - 35px);
        animation: animate-pulse 1.5s ease infinite;
        animation-delay: 2s
    }

    .phone-illustration__eyes, .phone-illustration__mouth {
        z-index: 3;
        animation: animate-eyes 1.5s ease forwards
    }

    .phone-illustration__mouth {
        top: 165px;
        width: 30px;
        left: calc(50% - 15px)
    }

    @keyframes animate-phone {
        0% {
            top: 150px
        }
        to {
            top: 78px
        }
    }

    @keyframes animate-eyes {
        0% {
            z-index: 1;
            opacity: 0
        }
        60% {
            opacity: 0
        }
        to {
            z-index: 3;
            opacity: 1
        }
    }

    @keyframes animate-background {
        0% {
            opacity: 0;
            top: 250px
        }
        50% {
            opacity: 0
        }
        to {
            opacity: 1;
            top: 42px
        }
    }

    @keyframes animate-pulse {
        0% {
            transform: scale(1.1)
        }
        50% {
            transform: scale(1)
        }
        to {
            transform: scale(1.1)
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
        .phone-illustration {
            top: 13px;
            left: 13px;
        }
        .phone-illustration__pocket {
            top: 126px;
            right: calc(50% - 67px);
            width: 132px;
            z-index: 2;
        }

        .phone-illustration__phone {
            width: 88px;
            left: calc(50% - 43px);
            top: 10px !important;
            animation: animate-phone 1.5s ease forwards
        }

        .phone-illustration__background {
            width: 170px;
            top: 25px;
            left: calc(50% - 81px);
            animation: animate-background-data-v-3065bd62 2s ease forwards;
        }

        .phone-illustration__eyes {
            width: 38px;
            top: 101px;
            left: calc(50% - 19px);
            animation: animate-pulse 1.5s ease infinite;
            animation-delay: 2s
        }

        .phone-illustration__eyes, .phone-illustration__mouth {
            z-index: 3;
            animation: animate-eyes 1.5s ease forwards
        }

        .phone-illustration__mouth {
            top: 116px;
            width: 16px;
            left: calc(50% - 8px);
        }

        @keyframes animate-phone {
            0% {
                top: 150px
            }
            100% {
                top: 70px
            }
        }

        @keyframes animate-eyes {
            0% {
                z-index: 1;
                opacity: 0
            }
            60% {
                opacity: 0
            }
            to {
                z-index: 3;
                opacity: 1
            }
        }

        @keyframes animate-background {
            0% {
                opacity: 0;
                top: 250px
            }
            50% {
                opacity: 0
            }
            to {
                opacity: 1;
                top: 42px
            }
        }

        @keyframes animate-pulse {
            0% {
                transform: scale(1.1)
            }
            50% {
                transform: scale(1)
            }
            to {
                transform: scale(1.1)
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
