<template>
    <div id="download">
        <div class="download-main" v-if="screenW>765">
            <div class="download-title">北极发卡网</div>
            <div class="download-content flex">
                <img src="../../assets/download-app.png">
                <div class="content-right">
                    <div class="download-t1">下载APP，管理你的店铺</div>
                    <div class="download-t2">支持消息推送，售前咨询，快捷查单等强大功能</div>
                    <div class="download-t3 flex">
                        <div class="t3-left">
                            <div class="t3-left1">IOS版下载</div>
                            <div>安卓版下载</div>
                        </div>
                        <div class="t3-right">
                            <img src="../../assets/download-core.png" width="227" height="227">
                            <div>扫描二维码下载</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="download-main-m" v-if="screenW<=765">
            <img src="../../assets/download-close.png" width="35" height="35" class="download-close">
            <img src="../../assets/download-title.png" width="100%" class="download-title">
            <img src="../../assets/download-remark.png" width="90%" class="download-remark">
            <img src="../../assets/download-close.png" width="35" height="35" class="download-close2">
            <img src="../../assets/download-app.png" width="100%" class="download-app">
        </div>
        <div class="download-bottom flex" v-if="screenW<=765">
            <div class="bottom-left">
                <img src="../../assets/download-core.png" width="100%">
                <div>扫描二维码下载</div>
            </div>
            <div class="bottom-right">
                <div style="margin-bottom: 10px">IOS版下载</div>
                <div>安卓版下载</div>
            </div>
        </div>
        <Footer v-if="screenW>765" />
    </div>
</template>

<script>
export default {
    name: 'Download',
    data() {
        return {
            screenW: null,
        }
    },
    mounted() {
        this.screenW = document.querySelector('html').offsetWidth;
    },
}
</script>

<style lang="scss">
#download {
    .download-main {
        background: #ff6050;
        color: #fff;
        padding-top: 93px;
        .download-title {
            font-size: 48px;
            margin-bottom: 142px;
            padding-left: 260px;
        }
        .download-content {
            justify-content: space-between;
            align-items: center;
            padding: 0 5%;
            >img {
                flex: 1;
                height: auto;
                margin-right: 100px;
            }
            .content-right {
                .download-t1 {
                    font-size: 65px;
                    margin-bottom: 33px;
                }
                .download-t2 {
                    font-size: 30px;
                    margin-bottom: 88px;
                }
                .download-t3 {
                    justify-content: space-between;
                    align-items: center;
                    .t3-left {
                        >div{
                            background: #fbc83c;
                            color: #ff5140;
                            display: flex;
                            flex-direction: column;
                            align-items: center;
                            justify-content: center;
                            width: 350px;
                            height: 71px;
                            font-size: 34px;
                            border-radius: 50px;
                            font-weight: 550;
                        }
                        .t3-left1 {
                            margin-bottom: 19px;
                        }
                    }
                    .t3-right {
                        font-size: 29px;
                        text-align: center;
                        >div {
                            margin-top: 29px;
                        }
                    }
                }
            }
        }
    }
    .download-main-m {
        padding: 32px 44px;
        background: #ff6050;
        color: #fff;
        .download-close {
            float: right;
        }
        .download-title {
            margin-top: 20px;
            margin-bottom: 11px;
            clear: both;
        }
        .download-remark {
            font-size: 13px;
            margin-bottom: 38px;
        }
        .download-close2 {
            margin-left: 11px;
        }
        .doanload-app {

        }
    }
    .download-bottom {
        justify-content: space-between;
        align-items: center;
        background: #fff;
        padding: 46px 32px;
        .bottom-left {
            text-align: center;
            flex: 1;
            margin-right: 20px;
            div {
                color: #474747;
                font-size: 10px;
                margin-top: 12px;
            }
        }
        .bottom-right {
            flex: 1;
            div {
                background: #fbc83c;
                color: #fff;
                border-radius: 50px;
                display: flex;
                justify-content: center;
                align-items: center;
                height: 35px;
                font-size: 13px;
            }
        }
    }
}
</style>