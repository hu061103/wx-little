<template>
  <div class="main">
    <div class="top-map"></div>
    <div class="beijing">
      <div class="userinfo">
        <div class="touxiang">
          <img src="../img/photo.png" alt />
        </div>
        <div class="xinxi">
          <p>倪庆</p>
          <p style="font-size:14px;color:#333;">
            <img src="../img/biao.png" alt /> 武汉HTML1906期
          </p>
        </div>
        <div class="tj">
          <p>统计</p>
        </div>
      </div>
      <div class="content">
        <div class="quan">
          <div class="one" style="font-weight: 600">签到</div>
          <div class="two" style="font-size:13px">14:40:12</div>
        </div>
        <div class="fanwei">已进入考勤范围</div>
        <div class="bottom-img">
          <img src="../img/jianying.jpg" alt />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import card from '@/components/card'

export default {
  data() {
    return {
      txt: "打卡首页"
      // motto: 'Hello miniprograme',
      // userInfo: {
      //   nickName: 'mpvue',
      //   avatarUrl: 'http://mpvue.com/assets/logo.png'
      // }
    };
  },

  components: {
    // card
  },

  methods: {
    // bindViewTap () {
    //   const url = '../logs/main'
    //   if (mpvuePlatform === 'wx') {
    //     mpvue.switchTab({ url })
    //   } else {
    //     mpvue.navigateTo({ url })
    //   }
    // },
    // clickHandle (ev) {
    //   console.log('clickHandle:', ev)
    //   // throw {message: 'custom test'}
    // }
  },

  created() {
    // let app = getApp()
  }
};
</script>

<style scoped>
.main {
  width: 100%;
  height: 100vh;
  /* background: red; */
  display: flex;
  flex-direction: column;
  position: relative;
}
.top-map {
  width: 100%;
  height: 40%;
  background-color: yellow;
}
.beijing {
  width: 100%;
  flex: 1;
  background: #d0e4fc;
  /* display: flex;
  justify-content: center; */
}
.userinfo {
  width: 98%;
  /* height: 150rpx; */
  height: 12%;
  background: #fff;
  border-radius: 15px;
  position: absolute;
  left: 0;
  right: 0;
  /* top: 0; */
  /* bottom: 620rpx; */
  bottom: 56%;
  margin: auto;
}
.content {
  width: 98%;
  /* height: 600rpx; */
  height: 54%;
  background-color: #fff;
  border-radius: 15px;
  position: absolute;
  left: 0;
  right: 0;
  /* top: 0; */
  bottom: 10rpx;
  margin: auto;
}
.touxiang {
  width: 15%;
  height: 70%;
  border: 2rpx solid #b6befa;
  border-radius: 50%;
  float: left;
  margin-top: 2%;
  margin-left: 30rpx;
}
.touxiang img {
  width: 100%;
  height: 100%;
}
.xinxi {
  float: left;
  margin-left: 30rpx;
  color: black;
  margin-top: 2%;
}
.xinxi img {
  width: 16px;
  height: 16px;
}
.tj {
  float: right;
  font-size: 20px;
  color: #4b8ff7;
  margin-right: 40rpx;
  margin-top: 5%;
}
.quan {
  width: 200rpx;
  height: 200rpx;
  border-radius: 50%;
  background: #498ef7;
  margin: 0 auto;
  margin-top: 40rpx;
  text-align: center;
  color: #fff;
  line-height: 80rpx;
}
.fanwei {
  width: 100%;
  text-align: center;
  margin-top: 30rpx;
  font-weight: 600;
}
.bottom-img {
  width: 100%;
  height: 190rpx;
  
  position: absolute;
  bottom: 10px;
}
.bottom-img img{
  width: 100%;
  height: 100%;
}
</style>
