<template>
    <div>
        <div class="modal-container">
            <div class="close" @click="hideModal">
                <img src="../../assets/img/close.svg">
            </div>
            <form>
                <h1 class="title modal-container__title">Contact us</h1>
                <input class="input modal-container__name" v-model="name" placeholder="Name">
                <input class="input modal-container__phone" v-model="phone" placeholder="+38 063 777 88 66">
                <input class="input modal-container__message" v-model="message" placeholder="Your message">
                <button class="button modal-container__button">Contact us</button>
            </form>
        </div>
    </div>
</template>

<script>
  export default {
    name: "ContactPopup",
    data() {
      return {
        name: '',
        phone: '',
        message: '',
      }
    },
    methods: {
      hideModal() {
        this.$emit('close')
      },
    },
  }
</script>

<style scoped lang="scss">
    .modal-container {
        padding: 40px 100px 70px 70px;
        background-color: #fff;
    }
    .input {
        width: 100%;
        display: block;
        margin: 15px 0 0 0;
        background-color: #f2f2f2;
        padding: 20px;
        -webkit-box-sizing: border-box;
        box-sizing: border-box;
        border: none;
        color: #888888;
        font-size: 14px;
        font-weight: 500;
        outline: none;
        &::placeholder {
            color: #888888;
            font-size: 14px;
            font-weight: 500;
        }
    }
    .button {
        outline: none;
        width: 100%;
        padding: 18px;
        border: none;
        font-size: 16px;
        color: #fff;
        font-weight: 600;
        margin: 15px 0 0 0;
        cursor: pointer;
        transition: .3s;
        background: #9b70fa; /* Old browsers */
        background: -moz-linear-gradient(-45deg, #9b70fa 0%, #590ff2 100%); /* FF3.6-15 */
        background: -webkit-linear-gradient(-45deg, #9b70fa 0%,#590ff2 100%); /* Chrome10-25,Safari5.1-6 */
        background: linear-gradient(135deg, #9b70fa 0%,#590ff2 100%); /* W3C, IE10+, FF16+, Chrome26+, Opera12+, Safari7+ */
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#9b70fa', endColorstr='#590ff2',GradientType=1 ); /* IE6-9 fallback on horizontal gradient */
        &:hover {
            transition: .3s;
            opacity: .9;
        }
    }
    .close {
        position: absolute;
        top: 30px;
        right: 30px;
        cursor: pointer;
        opacity: .8;
        transition: .3s;
        &:hover {
            opacity: 1;
            transition: .3s;
        }
    }
</style>
