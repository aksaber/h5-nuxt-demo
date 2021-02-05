<template>
    <div id="header">
        <div class="banner-bg" v-if="screenW>765">
            <span>北极发卡网欢迎您 ...</span>
        </div>
        <div class="banner flex" v-if="screenW>765">
            <img src="../assets/logo.png" alt="logo" class="banner-logo">
            <div class="banner-li flex">
                <li><nuxtLink to="/" :class="{active: index==0}">官网首页</nuxtLink></li>
                <li><nuxtLink to="charge" :class="{active: index==1}">收费模式</nuxtLink></li>
                <li><nuxtLink to="help" :class="{active: index==2}">帮助中心</nuxtLink></li>
                <li><nuxtLink to="api" :class="{active: index==3}">API收款接口服务</nuxtLink></li>
                <li><nuxtLink to="contactUs" :class="{active: index==4}">联系我们</nuxtLink></li>
            </div>
            <div class="banner-right flex">
                <div class="loginBtn flex">
                    <nuxtLink to="login">
                        <img
                            src="../assets/user-icon.png"
                            alt="用户"
                            width="28"
                            height="31"
                            style="margin-right: 23px; margin-left: -56px"
                        >登录/注册
                    </nuxtLink>
                </div>
                <div class="orderBtn flex">
                    <nuxtLink to="complaint">
                        <img
                            src="../assets/search-icon.png"
                            alt="搜索"
                            width="28"
                            height="28"
                            style="margin-right: 23px"
                        >订单查询/投诉
                    </nuxtLink>
                </div>
            </div>
        </div>
        <div class="banner-m flex" v-if="screenW<=765">
            <img src="../assets/logo-m.png" width="52" height="16">
            <img src="../assets/banner-right-m.png" width="20" height="16" @click="spreadList">
        </div>
        <div class="banner-li-m" v-if="screenW<=765 && listShow">
            <li><nuxtLink to="/">官网首页</nuxtLink></li>
            <li><nuxtLink to="charge">收费模式</nuxtLink></li>
            <li><nuxtLink to="help">帮助中心</nuxtLink></li>
            <li><nuxtLink to="api">API收款接口服务</nuxtLink></li>
            <li><nuxtLink to="contactUs">联系我们</nuxtLink></li>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Header',
    data() {
        return {
            index: 0,
            screenW: null,
            listShow: false
        }
    },
    mounted() {
        const name = this.$nuxt.$route.name;
        if (name == 'index') {
            this.index = 0;
        } else if (name == 'charge') {
            this.index = 1;
        } else if (name == 'help') {
            this.index = 2;
        } else if (name == 'api') {
            this.index = 3;
        } else if (name == 'contactUs') {
            this.index = 4;
        } else {
            this.index = null;
        }
        this.screenW = document.querySelector('html').offsetWidth;
    },
    methods: {
        spreadList() {
            this.listShow = !this.listShow;
        }
    }
}
</script>

<style lang="scss" scope>
#header {
    .banner-bg {
        background: url('../assets/header-banner.png') no-repeat;
        background-size: 100% 100%;
        height: 68px;
        line-height: 68px;
        padding: 0 10%;
        span {
            color: #fff;
        }
    }
    .banner {
        height: 156px;
        align-items: center;
        padding: 0 10%;
        justify-content: space-between;
        .banner-logo {
            width: 137px;
            height: 36px;
        }
        .banner-li {
            flex-direction: row;
            flex: 1;
            justify-content: center;
            li {
                margin: 0 2%;
                font-size: 20px;
            }
            a {
                color: #333;
            }
            .active {
                color: rgb(255, 96, 80);
                &:after {
                    content: '';
                    display: block;
                    width: 100%;
                    height: 2px;
                    border-bottom: 1px solid rgb(255, 96, 80);
                    margin-top: 10px;
                }
            }
        }
        .banner-right {
            .loginBtn {
                border: 1px solid #ccc;
                border-radius: 50px;
                font-size: 20px;
                width: 273px;
                height: 55px;
                line-height: 55px;
                align-items: center;
                justify-content: center;
                a {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    color: #333;
                }
            }
            .orderBtn {
                background: url('../assets/orderBtn.png') no-repeat;
                width: 239px;
                height: 55px;
                border-radius: 50px;
                font-size: 20px;
                align-items: center;
                justify-content: center;
                margin-left: -60px;
                a {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    color: #fff;
                }
            }
        }
    }
    .banner-m {
        background: url('../assets/banner-m.png') no-repeat;
        background-size: 100% 100%;
        height: 60px;
        justify-content: space-between;
        align-items: center;
        padding: 0 31px;
    }
    .banner-li-m {
        background: url('../assets/banner-m.png') no-repeat;
        background-size: 100% 100%;
        li {
            padding: 13px 31px 13px 20px;
            text-align: right;
            font-size: 16px;
            a {
                color: #fff;
            }
        }
    }
}
</style>