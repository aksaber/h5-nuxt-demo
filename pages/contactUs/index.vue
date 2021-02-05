<template>
    <div id="contactUs">
        <Header />
        <div class="contact-content">
            <div class="contact-top flex">
                <div class="topLeft flex">
                    <div class="top-radius">
                        <img src="../../assets/contact-message.png" width="72" height="68">
                    </div>
                    <div class="top-title">
                        <div class="top-t1">在线客服</div>
                        <div class="top-t2">客服QQ：139719871</div>
                        <div class="top-t2">工作时间：9:00-22:00</div>
                    </div>
                    <div class="top-border">
                        <img src="../../assets/contact-qq.png" width="22" height="24">
                        <span>前去咨询</span>
                    </div>
                </div>
                <div class="topRight flex">
                    <div class="top-radius">
                        <img src="../../assets/contact-kefu.png" width="81" height="83">
                    </div>
                    <div class="top-title">
                        <div class="top-t1">咨询电话</div>
                        <div class="top-t2">客服电话：400-283-1234</div>
                        <div class="top-t2">工作时间：9:00-22:00</div>
                    </div>
                </div>
            </div>
            <div class="contact-bottom flex">
                <div class="bottomLeft">
                    <div class="bottom-t1">北极发卡网有限公司</div>
                    <div class="bottom-t2">地址：什么市什么什么什么什么什么什么什么</div>
                    <div class="bottom-t2">邮编：38409318</div>
                </div>
                <div class="bottomRight"></div>
            </div>
            <Right style="position: absolute; bottom: -52px; right: calc(10% - 26px)" v-if="screenW>765" />
        </div>
        <Footer />
    </div>
</template>

<script>
export default {
    name: 'ContactUs',
    data() {
        return {
            screenW: null
        }
    },
    mounted() {
        this.screenW = document.querySelector('html').offsetWidth;
    }
}
</script>

<style lang="scss">
#contactUs {
    .contact-content {
        padding: 10px 10% 58px 10%;
        position: relative;
        @media screen and (max-width: 765px) {
            padding: 10px 5% 58px 5%;
        }
        .contact-top {
            justify-content: space-between;
            margin-top: 79px;
            margin-bottom: 79px;
            @media screen and (max-width: 765px) {
                margin-top: 56px;
                flex-direction: column;
                align-items: flex-start;
            }
            .topLeft {
                justify-content: space-evenly;
                align-items: center;
                width: 55%;
                @media screen and (max-width: 765px) {
                    width: 100%;
                    justify-content: unset;
                    margin-bottom: 22px;
                }
            }
            .topRight {
                justify-content: space-evenly;
                align-items: center;
                width: 45%;
                @media screen and (max-width: 765px) {
                    width: 100%;
                    justify-content: unset;
                }
            }
            .top-radius {
                background: url('../../assets/contact-radius.png') no-repeat;
                width: 154px;
                height: 154px;
                display: flex;
                justify-content: center;
                align-items: center;
                @media screen and (max-width: 765px) {
                    width: 66px;
                    height: 66px;
                    background-size: 100% 100%;
                    margin-top: -10px;
                    margin-right: 5%;
                }
                img {
                    @media screen and (max-width: 765px) {
                        width: 31px;
                        height: 31px;
                    }
                }
            }
            .top-title {
                margin-top: 20px;
                @media screen and (max-width: 765px) {
                    margin-top: 0;
                }
                .top-t1 {
                    font-size: 39px;
                    margin-bottom: 20px;
                    @media screen and (max-width: 765px) {
                        font-size: 16px;
                        margin-bottom: 9px;
                        font-weight: 550;
                    }
                }
                .top-t2 {
                    font-size: 20px;
                    margin-bottom: 10px;
                    @media screen and (max-width: 765px) {
                        font-size: 10px;
                    }
                }
            }
            .top-border {
                background: #ff6d4f;
                border-radius: 50px;
                color: #fff;
                display: flex;
                justify-content: space-evenly;
                align-items: center;
                width: 189px;
                height: 51px;
                padding: 0 29px;
                margin-top: -59px;
                @media screen and (max-width: 765px) {
                    width: 90px;
                    height: 22px;
                    padding: 0 12px;
                    font-size: 10px;
                    border-radius: 10px;
                    position: absolute;
                    right: 20px;
                }
                img {
                    @media screen and (max-width: 765px) {
                        width: 10px!important;
                        height: 10px!important;
                    }
                }
            }
        }
        .contact-bottom {
            justify-content: space-evenly;
            align-items: center;
            @media screen and (max-width: 765px) {
                flex-direction: column;
                align-items: flex-start;
            }
            .bottomLeft {
                .bottom-t1 {
                    font-size: 37px;
                    margin-bottom: 20px;
                    @media screen and (max-width: 765px) {
                        font-size: 25px;
                        margin-bottom: 14px;
                    }
                }
                .bottom-t2 {
                    font-size: 20px;
                    margin-bottom: 10px;
                    @media screen and (max-width: 765px) {
                        font-size: 15px;
                    }
                }
            }
            .bottomRight {
                background: #666;
                height: 361px;
                width: 60%;
                @media screen and (max-width: 765px) {
                    width: 100%;
                    height: 180px;
                    margin-top: 10px;
                }
            }
        }
    }
}
</style>