<template>
    <div id="charge">
        <Header />
        <div class="charge-content">
            <div class="charge-top flex">
                <div class="charge-topLeft">收取费率</div>
                <div class="charge-topTitle">
                    <div class="topTitle-top">4.00<span>%</span></div>
                    <div class="topTitle-bottom">默认费率</div>
                </div>
                <div class="charge-topRemark">
                    <div class="topRemark1">每天流水5W以上一天的商户</div>
                    <div>(根据各行各业不同情况，联系客服更改费率)</div>
                </div>
                <div class="charge-topRight">
                    <span>立即加入</span>
                    <img src="../../assets/charge-click.png" width="79" height="79">
                </div>
            </div>
            <div class="charge-bottom flex">
                <div class="bottom-list">
                    <div class="charge-bottomLeft">自动提现</div>
                    <img class="bottom-t1" src="../../assets/charge-word1.png" width="341" height="113">
                    <div class="bottom-t2">手续费/笔</div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>系统默认提现方式,无需申请</div>
                    </div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>每天下午3点前到账</div>
                    </div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>安全快捷</div>
                    </div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>满50元自动提现</div>
                    </div>
                    <div class="charge-bottomRight">
                        <span>立即加入</span>
                        <img src="../../assets/charge-click.png" width="79" height="79">
                    </div>
                </div>
                <div class="bottom-list">
                    <div class="charge-bottomLeft">资质认证</div>
                    <img class="bottom-t1" src="../../assets/charge-word2.png" width="393" height="96">
                    <div class="bottom-t2">手续费/笔</div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>每天流水稳定5W+的商家可申请</div>
                    </div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>满3000元每笔即时到账</div>
                    </div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>根据商家要求到账</div>
                    </div>
                    <div class="bottom-t3 flex">
                        <img src="../../assets/charge-sel.png" width="43" height="41">
                        <div>需联系北极卡客服审核开通</div>
                    </div>
                    <div class="charge-bottomRight">
                        <span>立即加入</span>
                        <img src="../../assets/charge-click.png" width="79" height="79">
                    </div>
                </div>
            </div>
            <Right style="float: right; margin-top: 14px; margin-right: -38px;" v-if="screenW>765" />
        </div>
        <Footer />
    </div>
</template>

<script>
export default {
    name: 'Charge',
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
#charge {
    .charge-content {
        padding: 100px 10% 55px 10%;
        @media screen and (max-width: 765px) {
            padding: 72px 2% 39px 2%;
        }
    }
    .charge-top {
        background: url('../../assets/charge-topBg.png') no-repeat;
        background-size: 100% 100%;
        height: 394px;
        position: relative;
        align-items: center;
        justify-content: space-evenly;
        color: #fff;
        @media screen and (max-width: 765px) {
            height: 197px;
            padding: 0 20px;
        }
        .charge-topLeft {
            position: absolute;
            left: -85px;
            top: 0;
            background: #fff;
            border-radius: 50px;
            color: #ff6b5c;
            font-size: 38px;
            width: 400px;
            height: 85px;
            line-height: 85px;
            text-align: center;
            padding-left: 80px;
            @media screen and (max-width: 765px) {
                font-size: 19px;
                width: 158px;
                height: 39px;
                line-height: 39px;
                padding-left: 41px;
                left: -2%;
            }
        }
        .charge-topTitle {
            @media screen and (max-width: 765px) {
                margin-top: -12px;
            }
            .topTitle-top {
                font-size: 113px;
                @media screen and (max-width: 765px) {
                    font-size: 51px;
                    margin-right: 5px;
                }
                span {
                    font-size: 28px;
                    @media screen and (max-width: 765px) {
                        font-size: 19px;
                    }
                }
            }
            .topTitle-bottom {
                font-size: 29px;
                @media screen and (max-width: 765px) {
                    font-size: 10px;
                }
            }
        }
        .charge-topRemark {
            @media screen and (max-width: 765px) {
                margin-top: -12px;
            }
            .topRemark1 {
                margin-bottom: 28px;
                @media screen and (max-width: 765px) {
                    margin-bottom: 8px;
                }
            }
            div {
                font-size: 29px;
                @media screen and (max-width: 765px) {
                    font-size: 10px;
                }
            }
        }
        .charge-topRight {
            position: absolute;
            right: -45px;
            bottom: 26px;
            background: #fff;
            border-radius: 50px;
            color: #ff6b5c;
            font-size: 34px;
            display: flex;
            width: 400px;
            justify-content: space-between;
            align-items: center;
            padding: 0 65px;
            height: 85px;
            @media screen and (max-width: 765px) {
                font-size: 16px;
                width: 181px;
                height: 39px;
                line-height: 39px;
                padding: 0 31px;
                right: -2%;
                bottom: 11px;
            }
            img {
                margin-top: 35px;
                @media screen and (max-width: 765px) {
                    width: 36px!important;
                    height: 36px!important;
                }
            }
        }
    }
    .charge-bottom {
        justify-content: space-between;
        margin-top: 35px;
        @media screen and (max-width: 765px) {
            margin-top: 16px;
            display: block;
        }
        .bottom-list {
            background: url('../../assets/charge-bottomBg.png') no-repeat;
            background-size: 100% 100%;
            height: 794px;
            color: #fff;
            position: relative;
            width: 47%;
            padding-top: 131px;
            padding-left: 8%;
            @media screen and (max-width: 765px) {
                height: 404px;
                padding-top: 62px;
                // width: 49%;
                width: 100%;
                margin-bottom: 16px;
            }
            .charge-bottomLeft {
                position: absolute;
                left: -85px;
                top: 0;
                background: #fff;
                border-radius: 50px;
                color: #ff6b5c;
                font-size: 38px;
                width: 400px;
                height: 85px;
                line-height: 85px;
                text-align: center;
                padding-left: 80px;
                @media screen and (max-width: 765px) {
                    left: -5%;
                    font-size: 18px;
                    width: 158px;
                    height: 39px;
                    line-height: 39px;
                    padding-left: 41px;
                }
            }
            .bottom-t1 {
                margin-bottom: 10px;
                @media screen and (max-width: 765px) {
                    width: 80%!important;
                    height: auto!important;
                }
                span {
                    font-size: 28px;
                }
            }
            .bottom-t2 {
                font-size: 29px;
                margin-bottom: 73px;
                @media screen and (max-width: 765px) {
                    font-size: 15px;
                    margin-bottom: 20px;
                }
            }
            .bottom-t3 {
                font-size: 28px;
                align-items: flex-end;
                margin-bottom: 47px;
                margin-left: -20px;
                @media screen and (max-width: 765px) {
                    font-size: 12px;
                    margin-bottom: 18px;
                    margin-left: -7px;
                }
                img {
                    margin-right: 20px;
                    @media screen and (max-width: 765px) {
                        width: 20px!important;
                        height: 18px!important;
                        margin-right: 8px;
                    }
                }
            }
            .charge-bottomRight {
                position: absolute;
                right: -45px;
                bottom: 0;
                background: #fff;
                border-radius: 50px;
                color: #ff6b5c;
                font-size: 34px;
                width: 400px;
                height: 85px;
                display: flex;
                justify-content: space-between;
                align-items: center;
                padding: 0 65px;
                @media screen and (max-width: 765px) {
                    right: -5%;
                    font-size: 16px;
                    width: 182px;
                    height: 39px;
                    line-height: 39px;
                    padding: 0 29px;
                }
                img {
                    @media screen and (max-width: 765px) {
                        width: 36px!important;
                        height: 36px!important;
                    }
                }
            }
        }
    }
}
</style>