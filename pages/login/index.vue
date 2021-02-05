<template>
    <div id="login">
        <Header v-if="screenW<=765" />
        <div class="login-bg flex">
            <img src="../../assets/login-bg2_.png" v-if="screenW>765">
            <div class="login-right">
                <div class="login-title">欢迎登录</div>
                <div class="login-account flex">
                    <img src="../../assets/login-account.png" width="45" height="41">
                    <input type="text" placeholder="用户名" v-if="screenW>765">
                    <span v-if="screenW<=765">用户名</span>
                </div>
                <input type="text" v-if="screenW<=765">
                <div class="login-account flex">
                    <img src="../../assets/login-psw.png" width="35" height="42" style="margin-let: 27px">
                    <input type="text" placeholder="登录密码" v-if="screenW>765">
                    <span v-if="screenW<=765">登录密码</span>
                </div>
                <input type="text" v-if="screenW<=765" style="margin-bottom: 30px">
                <div class="login-submit" v-if="screenW>765"><span>登录</span></div>
                <div class="login-select flex">
                    <div class="flex">
                        <div
                            :style="{background: isdui==0?'#ff6d4f':'#fff'}"
                            @click="selectDui(0)"
                        >
                            <img src="../../assets/login-dui.png" width="29" height="26">
                        </div>
                        <span>保存密码</span>
                    </div>
                    <div class="flex">
                        <div
                            :style="{background: isdui==1?'#ff6d4f':'#fff'}"
                            @click="selectDui(1)"
                        >
                            <img src="../../assets/login-dui.png" width="29" height="26">
                        </div>
                        <span>自动登录</span>
                    </div>
                </div>
                <div class="login-submit-m" v-if="screenW<=765">登录</div>
                <div class="login-register flex">
                    <div>注册账号</div>
                    <div>忘记密码</div>
                </div>
                <Right style="position: absolute; bottom: 0; right: -26px" v-if="screenW>765" />
                <Right style="position: absolute; bottom: 30%; right: -2%; top: unset" v-if="screenW<=765" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Login',
    data() {
        return {
            isdui: 0,
            screenW: null
        }
    },
    mounted() {
        this.screenW = document.querySelector('html').offsetWidth;
    },
    methods: {
        selectDui(index) {
            this.isdui = index;
        }
    }
}
</script>

<style lang="scss">
#login {
    width: 100%;
    height: 100vh;
    background: url('../../assets/login-bg.png') no-repeat;
    margin: 0 auto;
    @media screen and (max-width: 765px) {
        background-size: cover;
        height: auto;
    }
    .login-bg {
        // background: url('../../assets/login-bg2.png') no-repeat;
        // background-size: cover;
        height: 100vh;
        align-items: center;
        justify-content: center;
        @media screen and (max-width: 765px) {
            background: unset;
            width: 100%;
            height: auto;
            min-height: 100vh;
            display: block;
        }
        >img {
            height: 77%;
        }
        .login-right {
            background: #fff;
            border-radius: 50px;
            width: 45%;
            float: right;
            padding: 50px;
            position: relative;
            height: 77%;
            margin-left: -50px;
            @media screen and (max-width: 765px) {
                width: 95%;
                margin: 0 auto;
                margin-top: 62px;
                padding: 40px;
                float: unset;
                border-radius: 25px;
            }
            .login-title {
                color: #ff6d4f;
                font-size: 62px;
                text-align: center;
                margin-bottom: 81px;
                @media screen and (max-width: 765px) {
                    font-size: 28px;
                    margin-bottom: 50px;
                }
            }
            >input {
                background: #fff;
                border: 1px solid #e0e0e0;
                height: 38px;
                line-height: 38px;
                outline: none;
                width: 100%;
                font-size: 12px;
                margin-bottom: 12px;
                border-radius: 10px;
            }
            .login-account {
                align-items: center;
                margin-bottom: 40px;
                position: relative;
                @media screen and (max-width: 765px) {
                    margin-bottom: 12px;
                }
                input {
                    background: #fff;
                    border: 1px solid #fff;
                    height: 60px;
                    line-height: 60px;
                    outline: none;
                    width: 542px;
                    font-size: 24px;
                    @media screen and (max-width: 765px) {
                        height: 38px;
                        line-height: 38px;
                        width: 100%;
                        font-size: 12px;
                    }
                }
                &:after {
                    content: '';
                    display: block;
                    border-bottom: 1px solid #cac9c9;
                    height: 2px;
                    width: 100%;
                    position: absolute;
                    bottom: -32px;
                    @media screen and (max-width: 765px) {
                        height: 0;
                        border-bottom: 0
                    }
                }
                img {
                    margin-right: 22px;
                    margin-left: 19px;
                    @media screen and (max-width: 765px) {
                        width: 22px!important;
                        height: 20px!important;
                        margin-right: 11px;
                        margin-left: 3px;
                    }
                }
                span {
                    font-size: 12px;
                    color: #666;
                }
            }
            .login-submit {
                background: url('../../assets/login-button.png') no-repeat;
                height: 108px;
                line-height: 108px;
                width: 100%;
                color: #fff;
                font-size: 34px;
                margin-top: 46px;
                position: relative;
                margin-bottom: 34px;
                background-size: 100% 100%;
                span {
                    position: absolute;
                    top: -7px;
                    left: 50%;
                    margin-left: -34px;
                }
            }
            .login-submit-m {
                background: url('../../assets/login-button.png') no-repeat;
                width: 100%;
                color: #fff;
                margin-top: 46px;
                position: relative;
                margin-bottom: 34px;
                background-size: 100% 100%;
                height: 54px;
                line-height: 54px;
                font-size: 17px;
                display: flex;
                justify-content: center;
                align-items: center;
                padding-bottom: 5px;
            }
            .login-select {
                justify-content: space-evenly;
                margin-bottom: 69px;
                @media screen and (max-width: 765px) {
                    margin-bottom: 48px;
                }
                >div {
                    align-items: center;
                    >div {
                        background: #fff;
                        border: 1px solid #ccc;
                        border-radius: 10px;
                        width: 35px;
                        height: 35px;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        cursor: pointer;
                        margin-right: 13px;
                        @media screen and (max-width: 765px) {
                            height: 18px;
                            width: 18px;
                            margin-right: 6px;
                            border-radius: 4px;
                        }
                        img {
                            @media screen and (max-width: 765px) {
                                width: 14px!important;
                                height: 13px!important;
                            }
                        }
                    }
                    span {
                        font-size: 23px;
                        color: #838382;
                        @media screen and (max-width: 765px) {
                            font-size: 12px;
                        }
                    }
                }
            }
            .login-register {
                color: #ff7b60;
                justify-content: space-evenly;
                >div {
                    cursor: pointer;
                    @media screen and (max-width: 765px) {
                        font-size: 12px;
                    }
                    &:after {
                        content: '';
                        display: block;
                        height: 1px;
                        width: 100%;
                        padding-top: 10px;
                        border-bottom: 1px solid #ff7b60;
                    }
                }
            }
        }
    }
    ::-webkit-input-placeholder {
        color: #ccc;
    }
    ::-moz-placeholder {
        color: #ccc;
    }
    ::-ms-input-placeholder {
        color: #ccc;
    }
}
</style>