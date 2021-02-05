<template>
    <div id="agreement">
        <Header />
        <div class="agreement-content"></div>
        <div class="agreement-main">
            <div class="agreement-top flex">
                <div
                    v-for="(item, index) in data"
                    :key="index"
                    @click="select(index)"
                    :class="{active: index == type}"
                >{{item}}</div>
            </div>
            <div class="agreement-bottom">
                <div class="agreement-title">《{{data[type]}}》</div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
export default {
    name: 'Agreement',
    data() {
        return {
            data: ['隐私政策', '商品发布条例', '平台服务协议', '平台禁售商品目录'],
            screenW: null,
            type: 2
        }
    },
    mounted() {
        this.screenW = document.querySelector('html').offsetWidth;
    },
    methods: {
        select(index) {
            this.type = index;
        }
    }
}
</script>

<style lang="scss">
#agreement {
    .agreement-content {
        background: url('../../assets/agreement-bg.png') no-repeat;
        background-size: cover;
        background-position: 0 -100px;
        height: 800px;
        border-radius: 20px;
        padding-top: 500px;
        @media screen and (max-width: 765px) {
            height: 147px;
            padding-top: 0;
            border-radius: 0;
            background-position: center;
        }
    }
    .agreement-main {
        width: 74%;
        margin: 0 auto;
        @media screen and (max-width: 765px) {
            width: 100%;
        }
        .agreement-top {
            background: #ff6e4f;
            color: #fff;
            font-size: 29px;
            height: 96px;
            justify-content: space-evenly;
            align-items: center;
            border-top-left-radius: 20px;
            border-top-right-radius: 20px;
            @media screen and (max-width: 765px) {
                border-radius: 0;
                height: 40px;
                font-size: 10px;
                margin-top: -20px;
            }
            >div {
                cursor: pointer;
                height: 96px;
                line-height: 96px;
                padding: 0 2%;
                overflow: hidden;    
                text-overflow: ellipsis;    
                white-space: nowrap;
                @media screen and (max-width: 765px) {
                    height: 40px;
                    line-height: 40px;
                }
            }
        }
        .agreement-bottom {
            padding: 86px 10%;
            color: #666;
            height: 1200px;
            @media screen and (max-width: 765px) {
                padding: 24px 5%;
                height: 486px;
            }
            .agreement-title {
                font-size: 38px;
                text-align: center;
                @media screen and (max-width: 765px) {
                    font-size: 20px;
                }
            }
        }
    }
    .active {
        background: #fff;
        color: #ff6e4f;
    }
}
</style>