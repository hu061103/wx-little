<template>
    <div class="box">
        <div class="top">
           <img class="img1" src="../../../static/tabs/tb.png" alt="">
           <div class="xx">
               <div class="pic">
                   <img class="img2" src="../../../static/tabs/photo.png" alt="">
               </div>
                
               <div class="content">
                   <div class="div1">胡大大</div>
                    <div class="div2">武汉HTML5就业班1906期</div>
               </div>
           </div>
        </div>
        <div class="btn">
            <div class="xq">
                <img class="imgx" src="../../../static/images/xiao.png" alt="">
                <div class="wenzi">所在校区</div>
                <div class="right">武汉</div>
            </div>
            <div class="xq">
                <img class="imgb" src="../../../static/images/bai.png" alt="">
                <div class="wenzi">上课时间</div>
                <div class="right">09：00</div>
            </div>
            <div class="xq">
                <img class="imgy" src="../../../static/images/ye.png" alt="">
                <div class="wenzi">放学时间</div>
                <div class="right">21：00</div>
            </div>
        </div>

    </div>
</template>

<script>
export default {
    data(){
        return{
            msg:"vue"
        }
    },
    methods:{
        
    }
}
</script>
<style scoped>
    .box{
        display: flex;
        flex-direction: column;
    }
    .box .top{
        width: 100%;
        height: 125px;
        background: #2890ff;
        position: relative;
        margin-bottom: 45px;
    }
    .box .top .img1{
        width: 270px;
        height: 75px;
        display: block;
        margin-left: 20px;
    }
    .box .top .xx{
        height:100px;
        width: 90%;
        border-radius: 17px;
        position: absolute;
        top:75px;
        left:20px;
        z-index: 200;
        background: #fff;
        box-shadow: darkgrey 10px 10px 10px 5px ;
        padding: 15px;
        display: flex;
        flex-direction: row;
        box-sizing: border-box;
    }
    .box .top .xx .pic .img2{
        width: 70px;
        height: 70px;
        border: 4px solid #a8b1e2;
        border-radius: 50%;

    }
    .box .top .xx .content{
        margin-left: 15px;
        padding-top: 10px;
    }
    .box .top .xx .content .div1{
        font-size: 18px;
        font-weight: bolder;
        color: #323232;
        margin-bottom: 15px;
    }
    .box .top .xx .content .div2{
        font-size: 14px;
        color: #6b6b6b;
    }
    .box .btn{
        flex: 1;
        padding-left: 20px;
        padding-top: 20px;
        box-sizing: border-box;
    }
    .box .btn .xq{
        background: #fff;
        height: 55px;
        border-bottom: 1px solid #e5e5e5;
        display: flex;
        align-items: center;
        position: relative;
    }
    .box .btn .xq .imgx{
        width: 35px;
        height: 35px;
        border-radius: 50%;
        background: red;
    }
    .box .btn .xq .imgb{
        width: 35px;
        height: 35px;
        border-radius: 50%;
        background: #fec33d;
    }
    .box .btn .xq .imgy{
        width: 35px;
        height: 35px;
        border-radius: 50%;
        background: #9734d4;
    }
    .box .btn .xq .wenzi{
        margin-left: 10px;
        font-size: 18px;
        color: #666;
    }
    .box .btn .xq .right{
        position: absolute;
        font-size: 18px;
        right: 10px;
    }
</style>