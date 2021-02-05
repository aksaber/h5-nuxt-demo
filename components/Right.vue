<template>
    <div id="right">
        <div :class="['rightBorder', {'loginBorder': isLoginM}]" style="margin-bottom: 10px">
            <img src="../assets/qq-icon.png" width="24" height="26.5">
        </div>
        <div :class="['rightBorder', {'loginBorder': isLoginM}]">
            <img src="../assets/phone-icon.png" width="22" height="22">
        </div>
    </div>
</template>

<script>
export default {
    name: 'Right',
    data() {
        return {
            screenW: null,
            isLoginM: false
        }
    },
    mounted() {
        this.screenW = document.querySelector('html').offsetWidth;
        const router = this.$nuxt.$route.name;
        this.isLoginM = (this.screenW<=765 && router == 'login') ? true : false;
    }
}
</script>

<style lang="scss">
#right {
    @media screen and (max-width: 765px) {
        position: absolute;
        right: 25px;
        top: 39px;
    }
    .rightBorder {
        background: #ff6050;
        border-radius: 50%;
        width: 50px;
        height: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
        box-shadow: 0 0 10px #fff;
        @media screen and (max-width: 765px) {
            background: #ffb44b;
            // width: 90px;
            // height: 90px;
        }
        // img {
        //     @media screen and (max-width: 765px) {
        //         width: 44px!important;
        //         height: 47px!important;
        //     }
        // }
    }
    .loginBorder {
        background: #ff6050!important;
    }
}
</style>