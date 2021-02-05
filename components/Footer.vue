<template>
    <div id="footer" :class="{isDownload: router}">
        <div class="footer-top flex" v-if="screenW>765">
            <div class="footer-topLeft">
                <div class="footer-t1">企业联系方式</div>
                <div class="footer-t2 flex">
                    <img src="../assets/qq-footer.png" width="21" height="23" v-if="!router">
                    <img src="../assets/qq-footer-down.png" width="21" height="23" v-else>
                    <span>638197281212</span>
                </div>
                <div class="footer-t3">服务时间 10:00 - 22:00</div>
                <img src="../assets/sina-icon.png" width="30" height="29" class="footer-t4" v-if="!router">
                <img src="../assets/sina-icon-down.png" width="30" height="29" class="footer-t4" v-else>
                <div class="footer-t5">企业邮箱：391469186@qq.com</div>
            </div>
            <div class="footer-topCenter flex">
                <div class="footer-cLeft">
                    <img src="../assets/qrcode.png" width="76" height="76">
                    <div>扫码下载API</div>
                </div>
                <div class="footer-cLeft">
                    <img src="../assets/qrcode.png" width="76" height="76">
                    <div>扫码关注公众号</div>
                </div>
                <div class="footer-cRight">点击下载</div>
            </div>
            <div class="footer-topRight flex">
                <div class="footer-rList">
                    <div>买家服务</div>
                    <div>订单查询</div>
                    <div>订单投诉</div>
                    <div>投诉查询</div>
                    <div>帮助中心</div>
                </div>
                <div class="footer-rList">
                    <div>商户服务</div>
                    <div><nuxtLink to="login">商户登录</nuxtLink></div>
                    <div>注册商户</div>
                    <div>个人中心</div>
                    <div><nuxtLink to="download">APP下载</nuxtLink></div>
                </div>
                <div class="footer-rList">
                    <div>法律条款</div>
                    <div>隐私策略</div>
                    <div>商品发布条例</div>
                    <div><nuxtLink to="agreement">平台服务协议</nuxtLink></div>
                    <div>风控公示</div>
                </div>
                <div class="footer-rList">
                    <div>关于快发卡</div>
                    <div>联系我们</div>
                    <div>产品服务</div>
                    <div>禁售商品</div>
                </div>
            </div>
        </div>
        <div class="footer-top-m" v-if="screenW<=765">
            <Right />
            <img src="../assets/logo-m.png" width="80" height="22">
            <div class="line-m"></div>
            <div class="t1-m">企业Q<span></span>Q : 63819728</div>
            <div class="t1-m">企业邮箱 : 391469186@qq.com</div>
            <div class="t2-m">服务时间 : 10:00 - 22:00</div>
            <div class="t2-m flex">
                <div class="list-m">
                    <div>买家服务</div>
                    <div>订单查询</div>
                    <div>订单投诉</div>
                    <div>投诉查询</div>
                    <div>帮助中心</div>
                </div>
                <div class="list-m">
                    <div>商户服务</div>
                    <div><nuxtLink to="login">商户登录</nuxtLink></div>
                    <div>注册商户</div>
                    <div>个人中心</div>
                    <div><nuxtLink to="download">APP下载</nuxtLink></div>
                </div>
                <div class="list-m">
                    <div>法律条款</div>
                    <div>隐私策略</div>
                    <div>商品发布条例</div>
                    <div><nuxtLink to="agreement">平台服务协议</nuxtLink></div>
                    <div>风控公示</div>
                </div>
                <div class="list-m">
                    <div>关于快发卡</div>
                    <div>联系我们</div>
                    <div>产品服务</div>
                    <div>禁售商品</div>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="flex">
                <div>手机版请访问：M.KUAIFKA.COM</div>
                <div>版权所有：© 2016-2020 ALL RIGHTS RESERVED 深圳市木拉科技有限公司</div>
                <div>企业邮箱：800157060@B.QQ.COM</div>
            </div>
            <div class="flex">
                <div>TCP备案证书号：粤ICP备16032120号-1</div>
                <div>百度实名认证主体识别码：BDV-510600677</div>
                <div>网络文化经营许可证：粤网文[2017]8508-2021号 产品名称：快发卡</div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer',
    data() {
        return {
            screenW: null,
            router: null
        }
    },
    mounted() {
        this.screenW = document.querySelector('html').offsetWidth;
        if (this.$nuxt.$route.name == 'download') {
            this.router = 'download';
        }
    }
}
</script>

<style lang="scss" scope>
.isDownload {
    background: #fff!important;
    color: #333!important;
    .footer-cRight {
        background: #ff6050!important;
        color: #fff!important;
    }
    a {
        color: #333!important;
    }
}
#footer {
    background: url('../assets/footer-bg.png') no-repeat;
    background-size: 100% 100%;
    height: 535px;
    padding: 92px 0 37px;
    color: #fff;
    @media screen and (max-width: 765px) {
        padding: 0;
        height: auto;
        position: relative;
        background: #ff6050;
    }
    .footer-top {
        padding-bottom: 45px;
        border-bottom: 1px solid rgba(255, 255, 255, .3);
        padding-left: 5%;
        padding-right: 5%;
        justify-content: space-evenly;
        .footer-topLeft {
            .footer-t1 {
                font-size: 20px;
                margin-bottom: 42px;
            }
            .footer-t2 {
                font-size: 22px;
                margin-bottom: 39px;
                img {
                    margin-right: 17px;
                }
                span {
                    font-weight: 600;
                }
            }
            .footer-t3 {
                font-size: 16px;
                margin-bottom: 21px;
            }
            .footer-t4 {
                margin-bottom: 19px;
            }
            .footer-t5 {
                font-size: 18px;
            }
        }
        .footer-topCenter {
            justify-content: space-between;
            align-items: center;
            width: 30%;
            min-width: 400px;
            .footer-cLeft {
                display: flex;
                flex-direction: column;
                align-items: center;
                img {
                    margin-bottom: 25px;
                }
                div {
                    font-size: 12px;
                    text-align: center;
                }
            }
            .footer-cRight {
                background: #fff;
                border-radius: 12px;
                color: #ff786c;
                font-size: 19px;
                height: 42px;
                line-height: 42px;
                text-align: center;
                width: 174px;
                font-weight: 550;
            }
        }
        .footer-topRight {
            font-size: 16px;
            width: 30%;
            justify-content: space-between;
            .footer-rList {
                div {
                    margin-bottom: 36px;
                }
                a {
                    color: #fff;
                }
            }
        }
    }
    .footer-top-m {
        padding: 34px 34px 0px;
        >img {
            margin-bottom: 22px;
        }
        .line-m {
            width: 110%;
            height: 1px;
            border-bottom: 1px solid #adadad;
            margin-bottom: 36px;
            margin-left: -5%;
        }
        .t1-m {
            font-size: 17px;
            color: #feef01;
            margin-bottom: 21px;
            span {
                width: 9px;
                display: inline-block;
            }
        }
        .t2-m {
            margin-top: 21px;
            color: #fff;
            font-size: 17px;
            margin-bottom: 25px;
            justify-content: space-between;
            .list-m {
                font-size: 10px;
                div {
                    margin-bottom: 20px;
                }
                a {
                    color: #fff;
                }
            }
        }
    }
    .footer-bottom {
        padding-top: 41px;
        font-size: 12px;
        padding-left: 5%;
        padding-right: 5%;
        @media screen and (max-width: 765px) {
            padding-top: 36px;
            background: #333;
            padding-bottom: 32px;
        }
        .flex {
            margin-bottom: 15px;
            @media screen and (max-width: 765px) {
                flex-direction: column;
                text-align: center;
                margin-bottom: 0;
            }
            div {
                margin-right: 10px;
                @media screen and (max-width: 765px) {
                    margin-bottom: 14px;
                }
            }
        }
    }
}
</style>