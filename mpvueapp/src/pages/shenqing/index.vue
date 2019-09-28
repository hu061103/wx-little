<template>
    <div class="box">
        <div class="nav">
            <div class="tab">
                <div class="contain">
                    <div class="imgBox">
                        <img src="../../../static/images/qing.png" />
                    </div>
                </div>
                <p class="text">请假</p>
            </div>
            
            <div class="tab">
                <div class="contain">
                    <div class="imgBox" id="other">
                        <img src="../../../static/images/qian.png" />
                    </div>
                </div>
                <p class="text">补签</p>
            </div>
        </div>
        <div class="content">

            <div class="item">
                <div class="left">
                    <div class="imgBox">
                            <img src="../../../static/images/qing.png" />
                    </div>
                    <p>请假记录</p>
                </div>
                <span class="right">&gt;</span>
            </div>
            <div class="item" id="bto">
                <div class="left">
                    <div class="imgBox" id="other">
                            <img  src="../../../static/images/qian.png" />
                    </div>
                    <p>补签记录</p>
                </div>
                <span class="right">&gt;</span>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            msg:"shengqing"
        }
    }
}
</script>

<style scoped>

    .box{
        width: 100%;
        height: 100vh;
        background: #F5F8FF;
        /* flex: 1; */
        display: flex;
        flex-direction: column
    }
    .nav{
        width: 100%;
        height: 200rpx;
        display: flex;
        justify-content:space-around;
        align-items: center;
        background:#fff;
        margin-bottom: 20rpx;
    }
    .tab{
        width: 50%;
        height: 150rpx;
        text-align: center;
        /* line-height: 150rpx; */
    }
    .contain{
        width: 100%;
        height: 100rpx;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .imgBox{
        width: 100rpx;
        height: 100rpx;
        display: flex;
        align-items: center;
        justify-content: center;
        background: #F5715F;
        border-radius: 50%;
    }
    .tab img{
        width: 70rpx;
        height: 70rpx;
    }
    .tab p{
        margin-top: 15rpx;
        width: 100%;
        height: 35rpx;
    }
    .content{
        width: 100%;
        box-sizing: border-box;
        padding: 10rpx;
        height: 220rpx;
        background: #fff;
    }
    .content .item{
        width: 100%;
        height: 100rpx;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid #E4E4E4;

    }
    #bto{
        border: none;
    }
    #other{
        background: #FBA72C;
    }
    .content .item span{
        margin-right: 30rpx;
        color:#ccc; 
    }
    .content .item .left{
        width: 40%;
        height: 100rpx;
        display: flex;
        align-items: center;
    }
     .content .item .left p{
        /* margin-top: 10rpx; */
        width: 50%;
        height: 100rpx;
        line-height: 100rpx;
        text-align: center;
     }
     .content .item .left .imgBox{
         width: 70rpx;
         height: 70rpx;
         border-radius: 50%;
         margin-left: 20rpx;
        display: flex;
        align-items: center;
        margin-right: 10rpx;

     }
    .content .item .left img{
        width: 50rpx;
        height: 50rpx;
    }
</style>