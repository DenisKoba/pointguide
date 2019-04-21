<template>
    <div class="illustration">
        <transition name="fade">
            <PhoneIllustration />
        </transition>
    </div>
</template>

<script>
    import PhoneIllustration from './PhoneIllustration.vue'
  export default {
    name: "Illustrations",
    components: {
      PhoneIllustration
    }
  }
</script>

<style scoped lang="scss">
    .illustration {
        position: absolute;
        background-color: #fff;
        border-radius: 50%;
        left: 0;
        right: 0;
        margin: auto;
        height: 380px;
        width: 380px;
        top: 10px;
        display: flex;
        align-items: flex-end;
        justify-content: center;
        &__img {
            width: 250px;
            height: 250px;
            margin: 0 0 30px 0;
            animation: animate 9s forwards;
        }
    }

    @keyframes animate {
        0% {
            margin: 0 0 30px 0;
        }
        100% {
            margin: 0 0 60px 0;
            transform: scale(1.1);
        }
    }
</style>
