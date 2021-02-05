<template>
    <div id="help">
        <Header />
        <div class="help-content">
            <div class="help-top">
                <div class="top-content">
                    <div class="top-t1">帮助中心</div>
                    <div class="top-t2">我们提供了一些常见问题的解决方案</div>
                    <div class="top-t2">您可以在下方输入遇到的问题进行搜索</div>
                    <div class="top-t3" v-if="screenW>765">
                        <input type="text" placeholder="输入问题关键词 ..">
                        <div class="top-t3-button">
                            <span>问题查询</span>
                            <img src="../../assets/right-icon.png" width="13" height="23">
                        </div>
                    </div>
                </div>
            </div>
            <div class="top-t3-m" v-if="screenW<=765">
                <input type="text" placeholder="输入问题关键词 ..">
                <div class="top-t3-button">
                    <span>问题查询</span>
                    <img src="../../assets/right-icon.png" width="4" height="8">
                </div>
            </div>
            <div class="help-main">
                <div class="main-top flex">
                    <div class="top-list top-listIn">买家问题</div>
                    <div class="top-list">卖家问题</div>
                </div>
                <div class="main-bottom">
                    <textarea name="" id=""></textarea>
                    <textarea name="" id=""></textarea>
                    <textarea name="" id=""></textarea>
                    <textarea name="" id=""></textarea>
                    <textarea name="" id=""></textarea>
                    <textarea name="" id=""></textarea>
                </div>
                <Right style="position: absolute; bottom: 79px; right: 69px" v-if="screenW>765" />
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
export default {
    name: 'Help',
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
#help {
    .help-content {
        .help-top {
            background: url('../../assets/help-bg.png') no-repeat;
            background-size: 100% 100%;
            height: 800px;
            position: relative;
            background-position: center;
            @media screen and (max-width: 765px) {
                background: url('../../assets/help-bg-m.png') no-repeat;
                height: 131px;
                margin-top: 8px;
            }
            .top-content {
                position: absolute;
                right: 10%;
                bottom: 70px;
                text-align: right;
                @media screen and (max-width: 765px) {
                    right: 15px;
                    bottom: 0;
                }
                .top-t1 {
                    font-size: 75px;
                    color: #ff6f4f;
                    margin-bottom: 30px;
                    position: relative;
                    @media screen and (max-width: 765px) {
                        font-size: 22px;
                        font-weight: 550;
                        margin-bottom: 20px;
                    }
                    &:after {
                        content: '';
                        display: block;
                        background: url('../../assets/help-line.png') no-repeat;
                        width: 152px;
                        height: 3px;
                        position: absolute;
                        right: 0;
                        margin-top: 10px;
                        @media screen and (max-width: 765px) {
                            width: 33%;
                            height: 1.5px;
                        }
                    }
                }
                .top-t2 {
                    font-size: 24px;
                    margin-bottom: 10px;
                    @media screen and (max-width: 765px) {
                        font-size: 8px;
                        margin-bottom: 5px;
                    }
                }
                .top-t3 {
                    position: relative;
                    width: 668px;
                    margin-top: 30px;
                    @media screen and (max-width: 765px) {
                        width: 80%;
                        margin: 0 auto;
                        margin-top: 10px;
                    }
                    input {
                        background: #fff;
                        border-radius: 50px;
                        padding-left: 50px;
                        height: 87px;
                        line-height: 87px;
                        outline: none;
                        border: 1px solid #fff;
                        box-shadow: 0px 0px 10px #b3b1b1;
                        width: 668px;
                        @media screen and (max-width: 765px) {
                            width: 100%;
                            height: 32px;
                            line-height: 32px;
                            padding-left: 28px;
                        }
                    }
                    img {
                        margin-top: 5px;
                    }
                    span {
                        margin-left: 5px;
                    }
                    .top-t3-button {
                        background: #ff6f4f;
                        border-radius: 50px;
                        color: #fff;
                        font-size: 24px;
                        width: 204px;
                        display: flex;
                        align-items: center;
                        justify-content: space-between;
                        padding: 0 34px;
                        position: absolute;
                        right: 8px;
                        height: 72px;
                        bottom: 8px;
                        @media screen and (max-width: 765px) {
                            font-size: 10px;
                            width: 75px;
                            padding: 0 15px;
                            height: 26px;
                        }
                    }
                }
            }
        }
        .help-main {
            background: url('../../assets/help-main.png') no-repeat;
            background-size: cover;
            padding: 0 10%;
            padding-bottom: 48px;
            position: relative;
            @media screen and (max-width: 765px) {
                padding: 0 5%;
                padding-bottom: 15px;
            }
            .main-top {
                justify-content: space-evenly;
                .top-list {
                    font-size: 37px;
                    width: 40%;
                    text-align: center;
                    @media screen and (max-width: 765px) {
                        font-size: 12px;
                        width: 50%;
                    }
                }
                .top-listIn {
                    color: #ff6050;
                    &:after {
                        content: '';
                        display: block;
                        background: url('../../assets/help-bottomLine.png') no-repeat;
                        background-size: 100% 100%;
                        width: 80%;
                        height: 2px;
                        margin: 0 auto;
                        margin-top: 35px;
                        @media screen and (max-width: 765px) {
                            width: 100%;
                            margin-top: 10px;
                            height: 1px;
                        }
                    }
                }
            }
            .main-bottom {
                margin-top: 62px;
                @media screen and (max-width: 765px) {
                    margin-top: 15px;
                }
                textarea {
                    background: #fff;
                    border-radius: 35px;
                    height: 230px;
                    outline: none;
                    border: 1px solid #fff;
                    box-shadow: 0px 0px 4px #ccc;
                    margin-bottom: 20px;
                    width: 100%;
                    padding: 30px;
                    font-size: 30px;
                    resize: none;
                    @media screen and (max-width: 765px) {
                        height: 60px;
                        padding: 17px;
                        font-size: 12px;
                    }
                }
            }
        }
    }
    .top-t3-m {
        width: 80%;
        margin: 0 auto;
        margin-top: 10px;
        position: relative;
        margin-bottom: 15px;
        input {
            background: #fff;
            border-radius: 50px;
            padding-left: 28px;
            height: 32px;
            line-height: 32px;
            outline: none;
            border: 1px solid #fff;
            box-shadow: 0px 0px 10px #c1c1c1;
            width: 100%;
            font-size: 12px;
        }
        img {
            margin-top: 5px;
        }
        span {
            margin-left: 5px;
        }
        .top-t3-button {
            background: #ff6f4f;
            border-radius: 50px;
            color: #fff;
            font-size: 10px;
            width: 100px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 0 15px;
            position: absolute;
            right: 0;
            height: 32px;
            bottom: 0;

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