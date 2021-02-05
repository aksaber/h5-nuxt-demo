<template>
    <div id="home">
        <Header />
        <!-- top -->
        <section class="home-top">
            <div class="home-top-title">
                <span class="top-t1">北极发卡网</span>
                <span class="top-t2" v-if="screenW > 756">THE SERVICE/SYSTEM CAN BE CUSTOMIZED FOR FREE</span>
                <div class="top-t2-m" v-if="screenW <= 756">
                    <div>THE SERVICE/SYSTEM CAN BE</div>
                    <div>CUSTOMIZED FOR FREE</div>
                </div>
            </div>
            <div class="home-top-title2">
                <span class="top-t3">可免费定制服务/系统的</span>
            </div>
            <div class="top-t4">虚拟数字产品自动发货服务商</div>
            <div class="home-top-btn flex">
                <!-- <img src="../assets/top-word5.png" style="margin-left: 45px" > -->
                <span>注册成为商家</span>
                <div class="home-top-btn-border">
                    <img src="../assets/right-icon.png" >
                </div>
            </div>
            <div class="home-top-line" v-if="screenW>765"></div>
        </section>
        <!-- middle -->
        <section class="home-middle">
            <div class="flex" style="align-items: center">
                <div class="home-middle-title">核心优势 <span>/ CORE ADVANTAGES</span></div>
                <div class="home-middle-sTitle" v-if="screenW>765">
                    <div>支付宝、网银金额由系统自动打款到账</div>
                    <div>银行卡商户2个小时内到账</div>
                </div>
            </div>
            <div class="home-middle-sTitle-m" v-if="screenW<=765">
                <div>支付宝、网银金额由系统自动打款到账</div>
                <div>银行卡商户2个小时内到账</div>
            </div>
            <div class="home-middle-content flex">
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-zzxd.png" width="61" height="76" >
                    </div>
                    <div class="middle-content-title">自助下单</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">购买链接一键直达</div>
                </div>
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-qsfb.png" width="79" height="73" >
                    </div>
                    <div class="middle-content-title">轻松发布</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">一键发布商品简单快捷</div>
                </div>
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-zdjs.png" width="86" height="86" >
                    </div>
                    <div class="middle-content-title">自动结算</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">信誉无忧充分保障</div>
                </div>
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-mfdz.png" width="73" height="74" >
                    </div>
                    <div class="middle-content-title">免费定制</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">为商户免费开发页面</div>
                </div>
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-fwqq.png" width="94" height="94" >
                    </div>
                    <div class="middle-content-title">服务全球</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">购买链接一键直达</div>
                </div>
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-zykf.png" width="82" height="84" >
                    </div>
                    <div class="middle-content-title">专业客服</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">一键发布商品简单快捷</div>
                </div>
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-cxgx.png" width="79" height="65" >
                    </div>
                    <div class="middle-content-title">持续更新</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">信誉无忧充分保障</div>
                </div>
                <div class="middle-borderList flex">
                    <div class="middle-radius flex">
                        <img src="../assets/middle-zjbz.png" width="73" height="83" >
                    </div>
                    <div class="middle-content-title">资金保障</div>
                    <div class="middle-content-line"></div>
                    <div class="middle-content-remark">轻松设置商户信息</div>
                </div>
            </div>
            <div class="home-middle-bottom">API收款接口服务</div>
        </section>

        <!-- middle2 -->
        <section class="home-middle2 flex">
            <div class="home-middle2-left" v-if="screenW>765">
                <div style="margin-bottom: 45px">接收各类正规网站代收款服务，拥有专业技术开发团队，可以直接定制开发页面/系统</div>
                <div>通过SDK接入多种主流通道，用SAAS模式创建商户交易管理系统，您无须投入技术团队和通道资源也能够实现自己的支付系统、管理自己的交易订单</div>
            </div>
            <div class="home-middle2-right" v-if="screenW>765">
                <img src="../assets/middle2-radius1.png" class="middle2-radius1">
                <div class="middle2-border">点击此处了解更多</div>
                <img src="../assets/middle2-radius2.png" class="middle2-radius2">
            </div>
            <img src="../assets/middle2-bg1.png" class="middle2-bg1" v-if="screenW>765">
            <img src="../assets/middle2-bg2.png" class="middle2-bg2" v-if="screenW>765">
            <img src="../assets/middle2-bg3.png" class="middle2-bg3" v-if="screenW>765">
            <div v-if="screenW<=765" class="middle2-t1-m">接收各类正规网站代收款服务，拥有专业技术开发团队，可以直接定制开发页面/系统</div>
            <div v-if="screenW<=765" class="middle2-t2-m">通过SDK接入多种主流通道，用SAAS模式创建商户交易管理系统，您无须投入技术团队和通道资源也能够实现自己的支付系统、管理自己的交易订单</div>
        </section>

        <!-- middle3 -->
        <section class="home-middle3">
            <div class="home-middle3-title">平台功能 <span>/ PLATFORM FUNCTION</span></div>
            <div class="home-middle3-main flex">
                <div class="home-middle3-left flex">
                    <div class="middle3-bg1">
                        <span>卡密批量管理</span>
                        <img src="../assets/middle3-radius.png" >
                    </div>
                    <div class="middle3-bg2">
                        <span>卡密回收站</span>
                        <img src="../assets/middle3-radius.png" >
                    </div>
                    <div class="middle3-bg1">
                        <span>自定义购买页面</span>
                        <img src="../assets/middle3-radius.png" >
                    </div>
                    <div class="middle3-bg2">
                        <span>设置首先发卡</span>
                        <img src="../assets/middle3-radius.png" >
                    </div>
                </div>
                <div class="home-middle3-right">
                    <div class="middle3-title">众多支付通道</div>
                    <div class="middle3-remark">对接行业内众多最优质的支付通道，通道优质稳定，全力保障业务流畅</div>
                    <div class="middle3-img flex">
                        <img src="../assets/zfb.png" width="195" height="205" class="middle3-m1">
                        <img src="../assets/wechat.png" width="196" height="205" class="middle3-m2">
                        <img src="../assets/qq.png" width="186" height="185" class="middle3-m3">
                    </div>
                </div>
            </div>
            <div class="middle3-bottom">
                <img src="../assets/middle3-img.png" class="middle3-joinus">
                <div class="middle3-bottomTitle">赶快加入我们吧！</div>
                <div class="middle3-bottom-card flex">
                    <div class="middle3-cardlist">
                        <div class="middle3-cardlist-top cardlist1 flex">
                            <span class="middle3-cardtop-left">总共出售的卡</span>
                            <div v-if="screenW>400">
                                <div class="middle3-cardtop-right">CARDS SOLD</div>
                                <div class="middle3-cardtop-right">IN TOTAL</div>
                            </div>
                            <div class="middle3-cardtop-right" v-if="screenW<=400">CARDS SOLD IN TOTAL</div>
                        </div>
                        <div class="middle3-cardContent cardContent1">6666289<span>张</span></div>
                    </div>
                    <div class="middle3-cardlist">
                        <div class="middle3-cardlist-top flex">
                            <span class="middle3-cardtop-left">总共多少商户</span>
                            <div>
                                <div class="middle3-cardtop-right">HOW MANY MERCHANTS</div>
                                <div class="middle3-cardtop-right">IN TOTAL</div>
                            </div>
                        </div>
                        <div class="middle3-cardContent">666<span>家</span></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- middle4 -->
        <section class="home-middle4">
            <Right class="middle4-right" v-if="screenW>765" />
            <div class="home-middle4-title">消息中心 <span>/ MESSAGE CENTER</span></div>
            <div class="middle4-bg"></div>
            <div class="middle4-bottom flex" v-if="screenW>765">
                <div class="middle4-card">
                    <div class="middle4-cardTop">新闻中心</div>
                    <div class="middle4-cardContent">
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-more">了解更多 >>></div>
                    </div>
                </div>
                <div class="middle4-card">
                    <div class="middle4-cardTop" style="background: #ff6050">系统公告</div>
                    <div class="middle4-cardContent flex">
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-more">了解更多 >>></div>
                    </div>
                </div>
                <div class="middle4-card">
                    <div class="middle4-cardTop">结算公告</div>
                    <div class="middle4-cardContent flex">
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        <div class="middle4-more">了解更多 >>></div>
                    </div>
                </div>
            </div>
            <div class="middle4-bottom-m" v-if="screenW<=765">
                <div class="middle4-card middle4-card1">
                    <div class="middle4-cardTop">系统公告</div>
                    <div class="middle4-cardContent">
                        <div class="middle4-cardList cardListBig">【11-03】进博会开幕在即，六大看进博会开幕在...</div>
                        <div class="middle4-cardList cardListBig">【11-03】进博会开幕在即，六大看进博会开幕在...</div>
                        <div class="middle4-cardList cardListBig">【11-03】进博会开幕在即，六大看进博会开幕在...</div>
                        <div class="middle4-cardList cardListBig">【11-03】进博会开幕在即，六大看进博会开幕在...</div>
                    </div>
                </div>
                <div class="middle4-card2 flex">
                    <div class="middle4-card">
                        <div class="middle4-cardTop" style="background: #ff6050">新闻中心</div>
                        <div class="middle4-cardContent flex">
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        </div>
                    </div>
                    <div class="middle4-card">
                        <div class="middle4-cardTop">结算公告</div>
                        <div class="middle4-cardContent flex">
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                            <div class="middle4-cardList">【11-03】进博会开幕在即，六大看...</div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <Footer />
    </div>
</template>

<script>
export default {
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
#home {
    background-color: #fff;
    .home-top {
        background: url('../assets/top-bg.png') no-repeat;
        background-size: 100% 100%;
        height: 830px;
        padding-top: 183px;
        padding-left: 203px;
        color: #fff;
        @media screen and (max-width: 765px) {
            padding: 15% 5% 15% 10%;
            height: 400px;
            background-size: cover;
            background-position: center;
        }
        .home-top-title {
            margin-bottom: 20px;
            @media screen and (max-width: 765px) {
                display: flex;
                margin-bottom: 5px;
            }
            .top-t1 {
                margin-right: 5px;
                font-size: 48px;
                @media screen and (max-width: 765px) {
                    margin-right: 10px;
                    font-size: 24px;
                }
            }
            .top-t2 {
                font-size: 19px;
            }
            .top-t2-m {
                font-size: 11px;
            }
        }
        .home-top-title2 {
            margin-bottom: 10px;
            margin-left: -8px;
            .top-t3 {
                font-size: 70px;
                text-shadow: #797979 0px 6px 10px;
                @media screen and (max-width: 765px) {
                    font-size: 28px;
                    margin-left: 8px;
                }
            }
        }
        .top-t4 {
            margin-bottom: 59px;
            font-size: 39px;
            @media screen and (max-width: 765px) {
                font-size: 23px;
                margin-bottom: 18px;
            }
        }
        .home-top-btn {
            background: #fff;
            width: 287px;
            height: 61px;
            border-radius: 50px;
            align-items: center;
            justify-content: space-between;
            cursor: pointer;
            @media screen and (max-width: 765px) {
                width: 179px;
                height: 38px;
            }
            span {
                font-size: 24px;
                margin-left: 45px;
                color: #ff6050;
                @media screen and (max-width: 765px) {
                    font-size: 15px;
                    margin-left: 28px;
                }
            }
            .home-top-btn-border {
                background: #ff6050;
                width: 61px;
                height: 61px;
                border-radius: 50%;
                text-align: center;
                line-height: 67px;
                @media screen and (max-width: 765px) {
                    width: 37px;
                    height: 37px;
                    line-height: 37px;
                }
                img {
                    @media screen and (max-width: 765px) {
                        width: 7px!important;
                        height: 12px!important;
                    }
                }
            }
        }
        .home-top-line {
            width: 306px;
            height: 2px;
            opacity: 0.3;
            background: #fff;
            margin-top: 36px;
        }
    }
    
    .home-middle {
        background: url('../assets/middle-bg.png') no-repeat;
        background-size: 100% 100%;
        height: 1169px;
        padding-top: 94px;
        position: relative;
        @media screen and (max-width: 765px) {
            padding-top: 0;
            background: #fff;
            height: auto;
            padding-bottom: 65px;
        }
        .home-middle-title {
            background: url('../assets/middle-title1.png') no-repeat;
            color: #fff;
            width: 617px;
            height: 83px;
            line-height: 83px;
            font-size: 37px;
            text-align: center;
            padding-left: 138px;
            margin-right: 63px;
            @media screen and (max-width: 765px) {
                width: 100%;
                height: 49px;
                font-size: 22px;
                padding-left: 62px;
                margin-right: 0;
                text-align: left;
                line-height: 49px;
            }
            span {
                font-size: 24px;
                @media screen and (max-width: 765px) {
                    font-size: 14px;
                }
            }
        }
        .home-middle-sTitle {
            color: #a5a6a6;
            font-size: 20px;
        }
        .home-middle-sTitle-m {
            margin-top: 29px;
            padding-left: 62px;
            font-size: 12px;
            color: #7c7c7c;
            margin-bottom: 23px;
            padding-right: 62px;
        }
        .home-middle-content {
            padding-top: 117px;
            padding-left: 195px;
            flex-wrap: wrap;
            max-width: 1304px;
            @media screen and (max-width: 765px) {
                padding-left: 0;
                padding-top: 0;
                max-width: 100%;
                padding: 0 5%;
            }
            .middle-borderList {
                flex-direction: column;
                margin-right: 102px;
                @media screen and (max-width: 765px) {
                    margin-right: 0;
                    width: 33%;
                    padding-left: 5%;
                }
                .middle-radius {
                    background-image: linear-gradient(#ff854e, #ff8b4e);
                    border-radius: 50%;
                    margin-left: -4px;
                    width: 140px;
                    height: 140px;
                    margin-bottom: 46px;
                    align-items: center;
                    justify-content: center;
                    @media screen and (max-width: 765px) {
                        width: 47px;
                        height: 47px;
                        margin-left: 0;
                        margin-bottom: 15px;
                    }
                    img {
                        @media screen and (max-width: 765px) {
                            width: 21px!important;
                            height: 25px!important;
                        }
                    }
                }
                .middle-content-title {
                    font-size: 33px;
                    color: #6c6c6c;
                    margin-bottom: 18px;
                    @media screen and (max-width: 765px) {
                        font-size: 14px;
                        margin-bottom: 10px;
                    }
                }
                .middle-content-line {
                    height: 3px;
                    width: 59px;
                    background: #4083c4;
                    margin-bottom: 13px;
                    @media screen and (max-width: 765px) {
                        width: 40px;
                        margin-bottom: 8px;
                        height: 1px;
                    }
                }
                .middle-content-remark {
                    font-size: 20px;
                    color: #808080;
                    margin-bottom: 87px;
                    @media screen and (max-width: 765px) {
                        font-size: 10px;
                        margin-bottom: 29px;
                    }
                }
            }
        }
        .home-middle-bottom {
            background: url('../assets/middle-title2.png') no-repeat;
            max-width: 1245px;
            height: 115px;
            color: #fff;
            font-size: 57px;
            padding-left: 189px;
            line-height: 115px;
            position: absolute;
            width: 60%;
            bottom: 0;
            @media screen and (max-width: 765px) {
                width: 100%;
                font-size: 22px;
                height: 50px;
                line-height: 50px;
                padding-left: 62px;
            }
        }
    }

    .home-middle2 {
        background: #fff;
        padding: 85px 0 70px 231px;
        height: 407px;
        justify-content: space-between;
        align-items: center;
        position: relative;
        @media screen and (max-width: 765px) {
            height: auto;
            padding: 35px 61px;
            display: block;
        }
        .home-middle2-left {
            color: #666;
            font-size: 25px;
            max-width: 979px;
            width: 60%;
        }
        .home-middle2-right {
            position: relative;
            margin-bottom: 20px;
            margin-right: 8%;
        }
        .middle2-border {
            background: #ff6654;
            border-radius: 20px;
            color: #fff;
            width: 310px;
            height: 80px;
            font-size: 29px;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1;
            position: relative;
        }
        .middle2-radius1 {
            position: absolute;
            left: -25px;
            top: -25px;
            width: 61px;
            height: 61px;
        }
        .middle2-radius2 {
            position: absolute;
            right: -13px;
            bottom: -13px;
            width: 36px;
            height: 36px;
        }
        .middle2-bg1 {
            position: absolute;
            right: 0;
            top: -8px;
            width: 562px;
            height: 144px;
        }
        .middle2-bg2 {
            position: absolute;
            right: 0;
            top: 150px;
            width: 511px;
            height: 150px;
        }
        .middle2-bg3 {
            position: absolute;
            left: 0;
            bottom: -41px;
            width: 354px;
            height: 181px;
        }
        .middle2-t1-m {
            font-size: 16px;
            margin-bottom: 30px;
        }
        .middle2-t2-m {
            font-size: 16px;
        }
    }

    .home-middle3 {
        padding-bottom: 144px;
        @media screen and (max-width: 765px) {
            padding-bottom: 48px;
        }
        .home-middle3-title {
            background: url('../assets/middle-title1.png') no-repeat;
            background-size: 100% 100%;
            color: #fff;
            width: 100%;
            height: 83px;
            line-height: 83px;
            font-size: 38px;
            padding-left: 200px;
            @media screen and (max-width: 765px) {
                height: 53px;
                line-height: 53px;
                font-size: 23px;
                padding-left: 62px;
            }
            span {
                font-size: 24px;
                @media screen and (max-width: 765px) {
                    font-size: 15px;
                }
            }
        }
        .home-middle3-main {
            align-items: center;
            justify-content: space-between;
            padding-left: 126px;
            @media screen and (max-width: 765px) {
                padding: 35px 39px;
                flex-direction: column;
            }
        }
        .home-middle3-left {
            flex-direction: column;
            padding-top: 48px;
            max-width: 786px;
            width: 45%;
            @media screen and (max-width: 765px) {
                width: 100%;
                padding-top: 0;
                margin-bottom: 62px;
            }
            .middle3-bg1, .middle3-bg2 {
                height: 103px;
                color: #6e6a63;
                display: flex;
                align-items: center;
                justify-content: space-between;
                padding: 0 73px;
                @media screen and (max-width: 765px) {
                    height: 89px;
                    padding: 0 32px;
                }
                span {
                    font-size: 25px;
                    color: #333;
                    @media screen and (max-width: 765px) {
                        font-size: 16px;
                    }
                }
                img {
                    @media screen and (max-width: 765px) {
                        width: 19px;
                        height: 19px;
                    }
                }
            }
            .middle3-bg1 {
                background: #fef3da;
            }
            .middle3-bg2 {
                background: #fff8f7;
            }
        }
        .home-middle3-right {
            text-align: center;
            padding-right: 5%;
            padding-left: 2%;
            @media screen and (max-width: 765px) {
                padding-right: 0;
                padding-left: 0;
            }
            .middle3-title {
                color: #333;
                font-size: 48px;
                margin-bottom: 19px;
                @media screen and (max-width: 765px) {
                    font-size: 40px;
                    margin-bottom: 17px;
                    font-weight: 550;
                }
            }
            .middle3-remark {
                color: #787878;
                font-size: 21px;
                margin-bottom: 11px;
                text-align: left;
                @media screen and (max-width: 765px) {
                    font-size: 17px;
                    margin-bottom: 9px;
                    text-align: center;
                }
            }
            .middle3-img {
                justify-content: space-between;
                align-items: flex-end;
                .middle3-m1 {
                    @media screen and (max-width: 765px) {
                        width: 30%!important;
                        height: 30%!important;
                    }
                }
                .middle3-m2 {
                    @media screen and (max-width: 765px) {
                        width: 30%!important;
                        height: 30%!important;
                    }
                }
                .middle3-m3 {
                    @media screen and (max-width: 765px) {
                        width: 30%!important;
                        height: 30%!important;
                    }
                }
            }
        }
        .middle3-bottom {
            text-align: center;
            margin-top: 101px;
            @media screen and (max-width: 765px) {
                margin-top: 0;
            }
            .middle3-joinus {
                width: 607px;
                height: 82px;
                margin-bottom: 11px;
                @media screen and (max-width: 765px) {
                    width: 266px;
                    height: 41px;
                    margin-bottom: 2px;
                }
            }
            .middle3-bottomTitle {
                color: #333;
                font-size: 48px;
                margin-bottom: 56px;
                font-weight: 550;
                @media screen and (max-width: 765px) {
                    font-size: 21px;
                    margin-bottom: 23px;
                }
            }
            .middle3-bottom-card {
                justify-content: space-between;
                padding-left: 126px;
                padding-right: 126px;
                @media screen and (max-width: 765px) {
                    padding-left: 26px;
                    padding-right: 26px;
                }
                @media screen and (max-width: 400px) {
                    padding-left: 10px;
                    padding-right: 10px;
                }
                .middle3-cardlist {
                    background: url('../assets/home-cardBg.png') no-repeat;
                    background-size: 100% 100%;
                    color: #fff;
                    padding: 36px 33px 0;
                    height: 329px;
                    width: 48%;
                    @media screen and (max-width: 765px) {
                        height: 138px;
                        padding: 0 14px 0;
                        display: flex;
                        flex-direction: column;
                        justify-content: space-evenly;
                    }
                    @media screen and (max-width: 400px) {
                        width: 49%;
                        padding: 0 2px 0!important;
                    }
                    .cardlist1 {
                        @media screen and (max-width: 400px) {
                            margin-top: -10px;
                        }
                    }
                    .middle3-cardlist-top {
                        justify-content: space-between;
                        margin-bottom: 49px;
                        @media screen and (max-width: 765px) {
                            margin-bottom: 0px;
                        }
                        @media screen and (max-width: 400px) {
                            flex-wrap: wrap;
                            justify-content: center;
                        }
                        >div {
                            @media screen and (max-width: 400px) {
                                margin-top: 10px;
                            }
                        }
                        .middle3-cardtop-left {
                            background: #fff;
                            border-radius: 50px;
                            color: #ff6050;
                            font-size: 38px;
                            font-weight: 550;
                            text-align: center;
                            width: 281px;
                            height: 70px;
                            line-height: 70px;
                            @media screen and (max-width: 765px) {
                                font-size: 12px;
                                width: 122px;
                                height: 16px;
                                line-height: 16px;
                            }
                            @media screen and (max-width: 400px) {
                                font-size: 10px;
                                min-width: 100px;
                            }
                        }
                        .middle3-cardtop-right {
                            font-size: 18px;
                            text-align: right;
                            @media screen and (max-width: 765px) {
                                font-size: 9px;
                            }
                        }
                    }
                    .cardContent1 {
                        @media screen and (max-width: 400px) {
                            margin-bottom: 0px!important;
                        }
                    }
                    .middle3-cardContent {
                        font-size: 76px;
                        font-weight: 600;
                        @media screen and (max-width: 765px) {
                            font-size: 33px;
                            margin-bottom: 10px;
                        }
                        @media screen and (max-width: 400px) {
                            font-size: 23px;
                        }
                        span {
                            margin-left: 10px;
                            font-size: 28px;
                            @media screen and (max-width: 765px) {
                                font-size: 13px;
                                margin-left: 2px;
                            }
                        }
                    }
                }
            }
        }
    }

    .home-middle4 {
        position: relative;
        padding-bottom: 48px;
        @media screen and (max-width: 765px) {
        }
        .middle4-right {
            position: absolute;
            right: 52px;
            top: -26px;
            z-index: 1;
        }
        .home-middle4-title {
            background: url('../assets/middle-title1.png') no-repeat;
            color: #fff;
            width: 617px;
            height: 83px;
            line-height: 83px;
            font-size: 38px;
            text-align: center;
            padding-left: 140px;
            margin-right: 63px;
            position: relative;
            z-index: 1;
            @media screen and (max-width: 765px) {
                width: 100%;
                height: 56px;
                line-height: 56px;
                padding-left: 62px;
                margin-right: 0;
                font-size: 23px;
                text-align: left;
            }
            span {
                font-size: 24px;
                @media screen and (max-width: 765px) {
                    font-size: 15px;
                }
            }
        }
        .middle4-bg {
            background: url('../assets/middle4-bg.png') no-repeat;
            background-size: cover;
            width: 100%;
            height: 503px;
            position: absolute;
            top: 0;
            left: 0;
            @media screen and (max-width: 765px) {
                height: 260px;
                background-size: 100% 100%;
                top: 56px;
            }
        }
        .middle4-bottom {
            margin-top: 316px;
            justify-content: space-between;
            position: relative;
            padding: 0 168px;
            .middle4-card {
                border-radius: 10px;
                width: 30%;
                height: 450px;
                box-shadow: 0px 0px 10px #a59999;
                .middle4-cardTop {
                    background: #ff8073;
                    color: #fff;
                    text-align: center;
                    height: 107px;
                    line-height: 107px;
                    font-size: 34px;
                    border-top-left-radius: 10px;
                    border-top-right-radius: 10px;
                }
                .middle4-cardContent {
                    padding-top: 61px;
                    padding-bottom: 30px;
                    padding-left: 30px;
                    padding-right: 30px;
                    color: #717171;
                    flex-direction: column;
                    .middle4-cardList {
                        margin-bottom: 18px;
                        overflow: hidden;    
                        text-overflow: ellipsis;    
                        white-space: nowrap;
                        &:after {
                            content: '';
                            border-bottom: 1px dashed #666;
                            height: 1px;
                            display: block;
                            padding-bottom: 18px;
                        }
                    }
                    .middle4-more {
                        margin-bottom: 18px;
                    }
                }
            }
        }
        .middle4-bottom-m {
            margin-top: 171px;
            position: relative;
            .middle4-card1 {
                width: 90%!important;
                margin: 0 auto;
                margin-bottom: 10px;
            }
            .middle4-card2 {
                width: 90%!important;
                margin: 0 auto;
                margin-bottom: 10px;
                justify-content: space-between;
            }
            .middle4-card {
                border-radius: 10px;
                width: 48%;
                height: 300px;
                box-shadow: 0px 0px 10px #a59999;
                .middle4-cardTop {
                    background: #ff8073;
                    color: #fff;
                    text-align: center;
                    height: 74px;
                    line-height: 74px;
                    font-size: 20px;
                    border-top-left-radius: 10px;
                    border-top-right-radius: 10px;
                }
                .middle4-cardContent {
                    padding-top: 36px;
                    padding-bottom: 30px;
                    padding-left: 8%;
                    padding-right: 8%;
                    color: #717171;
                    flex-direction: column;
                    background: #fff;
                    .cardListBig {
                        font-size: 16px!important;
                    }
                    .middle4-cardList {
                        margin-bottom: 7px;
                        overflow: hidden;    
                        text-overflow: ellipsis;    
                        white-space: nowrap;
                        font-size: 12px;
                        &:after {
                            content: '';
                            border-bottom: 1px dashed #666;
                            height: 1px;
                            display: block;
                            padding-bottom: 11px;
                        }
                    }
                }
            }
        }
    }
}
</style>
