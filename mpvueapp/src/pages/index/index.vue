<template>
  <div class="main">
    <div class="top-map">
      <map
        id="map"
        longitude="114.434897"
        latitude="30.46387"
        scale="14"
        show-location
        style="width: 100%; height: 100%;"
        :markers="markers"
      ></map>
    </div>

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
          <div id="time" class="two" style="font-size:13px"> {{date}} </div>
        </div>
        <div class="fanwei">已进入考勤范围 {{juli}}</div>

        <div class="bottom-img">
          <img src="../img/jianying.jpg" alt />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      txt: "打卡首页",
      markers: [{
      iconPath: require("../img/gongsi.png"),
      id: 0,
      latitude: '30.45829881923435',
      longitude: '114.42828465912626',
      width: 50,
      height: 50
    }],
    juli:0,
    timer:null,
    date:""
    };
  },

  components: {
    // card
  },
  mounted() {
    var that = this;
    mpvue.getLocation({
      type: "wgs84",
      success: res => {
        const latitude = res.latitude;
        const longitude = res.longitude;
        const speed = res.speed;
        const accuracy = res.accuracy;
        console.log(latitude,longitude);
        that.GetDistance(30.45829881923435,114.42828465912626,latitude,longitude)
        
      }
    });
     this.timer = setInterval(() => {
      this.show(); // 修改数据date
    }, 1000);
    
 },
 
   beforeDestroy() {
    if (this.timer) {
      clearInterval(this.timer); // 在Vue实例销毁前，清除我们的定时器
    }
  },
  methods: {
    GetDistance(lat1, lng1, lat2, lng2) {
      var radLat1 = lat1 * Math.PI / 180.0;
      var radLat2 = lat2 * Math.PI / 180.0;
      var a = radLat1 - radLat2;
      var b = lng1 * Math.PI / 180.0 - lng2 * Math.PI / 180.0;
      var s =
        2 *
        Math.asin(
          Math.sqrt(
            Math.pow(Math.sin(a / 2), 2) +
              Math.cos(radLat1) *
                Math.cos(radLat2) *
                Math.pow(Math.sin(b / 2), 2)
          )
        );
      s = s * 6378.137; // EARTH_RADIUS;
      s = Math.round(s * 10000) / 10000;
      console.log(s);
      console.log(lat2, "---" + lng2);
      this.juli = s;
    },
    show() {
      var d = new Date();
      var h = d.getHours(); // 16下午4点     24小时制
      var m = d.getMinutes(); //31分
      var s = d.getSeconds(); //50秒
      s= s<10?'0'+s:s
      this.date = `${h}:${m}:${s}`;
    }
  },

  created() {
    
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
.bottom-img img {
  width: 100%;
  height: 100%;
}
</style>
