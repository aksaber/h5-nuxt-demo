<template>
    <div id="complaint">
        <Header />
        <div class="complaint-content">
            <div class="complaint-list flex">
                <div class="complaint-left flex">
                    <div class="complaint-title">
                        <div class="complaintTitle">查询类型</div>
                        <div class="complaintSelect flex">
                            <span>订单查询</span>
                            <img src="../../assets/complaint-play.png" width="15" height="11">
                        </div>
                    </div>
                    <div class="complaint-input">
                        <div class="complaintTitle">订单号</div>
                        <div class="complaintInput flex">
                            <img src="../../assets/complaint-search.png" width="20" height="20">
                            <input type="text" placeholder="请输入订单号">
                        </div>
                    </div>
                </div>
                <div class="complaint-right flex">
                    <span>订单查询</span>
                    <img src="../../assets/complaint-click.png" width="54" height="54">
                </div>
            </div>
            <div class="complaint-list flex">
                <div class="complaint-left left2 flex">
                    <div class="complaint-title">
                        <div class="complaintTitle">查询类型</div>
                        <div class="complaintSelect flex">
                            <span>投诉查询</span>
                            <img src="../../assets/complaint-play.png" width="15" height="11">
                        </div>
                    </div>
                    <div class="complaint-input">
                        <div class="complaintTitle">订单号</div>
                        <div class="complaintInput flex">
                            <img src="../../assets/complaint-search.png" width="20" height="20">
                            <input type="text" placeholder="请输入订单号">
                        </div>
                    </div>
                </div>
                <div class="complaint-right right2 flex">
                    <span>查询投诉</span>
                    <img src="../../assets/complaint-click.png" width="54" height="54">
                </div>
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
export default {
    name: 'Complaint'
}
</script>

<style lang="scss">
#complaint {
    .complaint-content {
        padding: 20px 10% 65px 10%;
        @media screen and (max-width: 765px) {
            padding: 20px 0;
        }
        .complaint-list {
            .complaint-left {
                background: url('../../assets/complaint-border.png') no-repeat;
                background-size: 100% 100%;
                height: 265px;
                color: #fff;
                flex: 1;
                align-items: center;
                padding-left: 85px;
                @media screen and (max-width: 765px) {
                    height: 77px;
                    padding-left: 33px;
                }
                .complaint-title {
                    margin-right: 31px;
                    margin-top: -16px;
                    @media screen and (max-width: 765px) {
                        margin-right: 7px;
                        margin-top: -5px;
                    }
                }
                .complaint-input {
                    width: 58%;
                    margin-top: -16px;
                    @media screen and (max-width: 765px) {
                        margin-top: -6px;
                    }
                }
            }
            .complaint-right {
                background: url('../../assets/complaint-radius.png') no-repeat;
                background-size: 100% 100%;
                height: 265px;
                width: 375px;
                font-size: 48px;
                color: #fff;
                align-items: center;
                justify-content: center;
                position: relative;
                @media screen and (max-width: 765px) {
                    width: 100px;
                    height: 77px;
                    font-size: 12px;
                }
                span {
                    margin-top: -10px;
                    cursor: pointer;
                    @media screen and (max-width: 765px) {
                        margin-top: -5px;
                    }
                }
                img {
                    position: absolute;
                    bottom: 37px;
                    right: 48px;
                    @media screen and (max-width: 765px) {
                        width: 13px!important;
                        height: 13px!important;
                        bottom: 15px;
                        right: 12px;
                    }
                }
            }
            .complaintTitle {
                font-size: 28px;
                margin-bottom: 31px;
                margin-left: 11px;
                @media screen and (max-width: 765px) {
                    font-size: 8px;
                    margin-bottom: 6px;
                    margin-left: 5px;
                }
            }
            .complaintSelect {
                background: #fff;
                border-radius: 10px;
                height: 73px;
                color: #777;
                font-size: 22px;
                align-items: center;
                justify-content: space-between;
                padding: 0 27px;
                @media screen and (max-width: 765px) {
                    height: 30px;
                    font-size: 8px;
                    padding: 0 7px;
                    justify-content: center;
                    border-radius: 5px;
                }
                span {
                    margin-right: 11px;
                    cursor: pointer;
                    @media screen and (max-width: 765px) {
                        margin-right: 0;
                    }
                }
                img {
                    margin-top: 5px;
                    cursor: pointer;
                    @media screen and (max-width: 765px) {
                        display: none;
                    }
                }
            }
            .complaintInput {
                align-items: center;
                padding: 0 29px;
                background: #fff;
                border-radius: 10px;
                @media screen and (max-width: 765px) {
                    border-radius: 5px;
                    padding: 0 7px;
                }
                img {
                    margin-right: 17px;
                    @media screen and (max-width: 765px) {
                        width: 4px!important;
                        height: 4px!important;
                        margin-right: 7px;
                    }
                }
                input {
                    background: #fff;
                    border-radius: 10px;
                    height: 73px;
                    line-height: 73px;
                    outline: none;
                    border: 1px solid #fff;
                    @media screen and (max-width: 765px) {
                        height: 30px;
                        line-height: 30px;
                        border-radius: 5px;
                        width: 100%;
                        font-size: 12px;
                    }
                }
            }
            .left2 {
                background: url('../../assets/complaint-border2.png') no-repeat;
                background-size: 100% 100%;
            }
            .right2 {
                background: url('../../assets/complaint-radius2.png') no-repeat;
                background-size: 100% 100%;
            }
        }
    }
    ::-webkit-input-placeholder {
        color: #808183;
    }
    ::-moz-placeholder {
        color: #808183;
    }
    ::-ms-input-placeholder {
        color: #808183;
    }
}
</style>