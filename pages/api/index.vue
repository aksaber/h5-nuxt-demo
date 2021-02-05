<template>
    <div id="api">
        <Header />
        <div class="api-content">
            <div v-for="item in program" :key="item.id" class="api-list">
                <div class="api-title">{{item.title}}</div>
                <div class="api-mainFlex flex">
                    <div v-for="(item2, index) in item.platform" :key="index" class="api-main flex">
                        <div class="api-name">{{item2}}</div>
                        <div class="api-more">查看更新日志</div>
                    </div>
                    <div v-if="item.id == 1" class="api-button">
                        <span>点击了解更多</span>
                        <img src="../../assets/api-right.png" width="17" height="21">
                    </div>
                </div>
            </div>
            <div class="api-bottom">了解如何使用，请阅读开发指南 ></div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Api',
    data() {
        return {
            program: [
                {
                    id: 1,
                    title: 'Server SDK_ （常用语言）',
                    platform: ['PHP', 'Java', 'Node.js', 'Go', 'Python', 'Ruby', '其他等各类语言']
                },
                {
                    id: 2,
                    title: 'Client SDK_',
                    platform: ['iOS', 'Android', 'HTML5']
                },
                {
                    id: 3,
                    title: '其他平台 SDK_',
                    platform: ['APICloud', 'AppCan', 'Cordova', 'React Native']
                },
            ]
        }
    }
}
</script>

<style lang="scss">
#api {
    .api-content {
        background: url('../../assets/api-bg.png') no-repeat;
        background-size: cover;
        padding-top: 156px;
        padding-left: 10%;
        padding-right: 10%;
        padding-bottom: 137px;
        color: #fff;
        @media screen and (max-width: 765px) {
            padding-top: 70px;
            padding-left: 5%;
            padding-right: 2%;
            padding-bottom: 40px;
        }
        .api-list {
            margin-bottom: 29px;
            .api-title {
                font-size: 31px;
                margin-bottom: 30px;
                @media screen and (max-width: 765px) {
                    font-size: 20px;
                }
            }
            .api-mainFlex {
                flex-wrap: wrap;
                position: relative;
                .api-main {
                    background: #333;
                    width: 256px;
                    height: 152px;
                    padding: 35px 46px 30px 46px;
                    flex-direction: column;
                    justify-content: space-between;
                    margin-right: 36px;
                    margin-bottom: 40px;
                    @media screen and (max-width: 765px) {
                        width: 30%;
                        padding: 13px 17px;
                        height: auto;
                        margin-right: 3%;
                        margin-bottom: 4%;
                    }
                    .api-name {
                        font-size: 20px;
                        @media screen and (max-width: 765px) {
                            font-size: 14px;
                            margin-bottom: 30px;
                        }
                    }
                    .api-more {
                        color: #939393;
                        font-size: 14px;
                        @media screen and (max-width: 765px) {
                            font-size: 12px;
                        }
                    }
                }
                .api-button {
                    position: absolute;
                    bottom: 40px;
                    right: 0;
                    background: url('../../assets/api-border.png') no-repeat;
                    width: 255px;
                    height: 57px;
                    display: flex;
                    justify-content: space-evenly;
                    align-items: center;
                    color: #fff;
                    font-size: 25px;
                    @media screen and (max-width: 765px) {
                        width: 167px;
                        height: 45px;
                        font-size: 15px;
                        bottom: 6%;
                        right: 4%;
                    }
                    img {
                        @media screen and (max-width: 765px) {
                            width: 14px!important;
                            height: 14px!important;
                        }
                    }
                    span {
                        margin-top: -5px;
                        @media screen and (max-width: 765px) {
                            margin-top: 0;
                        }
                    }
                }
            }
        }
        .api-bottom {
            font-size: 26px;
            text-align: center;
            @media screen and (max-width: 765px) {
                display: none;
            }
        }
    }
}
</style>