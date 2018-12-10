<template>
  <div class="container">
    <!-- <div class="ct-title">
      <div :class="{ctname1:isA,ctname11:!isA}" @click="toggle">专辑</div>
      <div :class="{ctname2:isB,ctname22:!isB}" @click="toggle1">栏目</div>
    </div>-->
    <div class="ct-new-tab">
      <div class="tab-title" :class="{'tab-active':activeIndex==0}" @click="getData(0)">
        <span class="tat">专辑</span>
      </div>
      <div class="tab-title" :class="{'tab-active':activeIndex==1}" @click="getData(1)">
        <span class="tat">栏目</span>
      </div>
    </div>
    <!-- <switch checked bindchange="switch1Change"/>
    <switch bindchange="switch2Change"/>-->
    <scroll-view scroll-y>qwe
      <map id="map" longitude="118.78" latitude="32.04"></map>
    </scroll-view>

    <div class="ct-body">
      <div class="ctb-container" v-for="list in entry" :key="index">
        <div class="ctb-img">
          <img :src="list.img" class="ctb">
          <div class="ctb-title">{{list.title}}</div>
        </div>
        <div @click="clickMe" class="ctb-content">{{list.content}}</div>
        <div class="ctb-de">{{list.de}}</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      activeIndex: null,
      entry: [
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-001.png",
          title: "大公司",
          content: "+关注",
          de: "竞争趋势 互联网大公司的寒冬要来了 各个巨头互联网..."
        },
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-002.png",
          title: "汽车交通",
          content: "+关注",
          de: "汽车在线报道最新路况信息 为您快速导航 避免拥..."
        },
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-003.png",
          title: "商业精选",
          content: "+关注",
          de: "竞争趋势 互联网大公司的寒冬要来了 各个巨头互联网..."
        },
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-004.png",
          title: "区块链",
          content: "+关注",
          de: "汽车在线报道最新路况信息 为您快速导航 避免拥..."
        },
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-005.png",
          title: "人工智能",
          content: "+关注",
          de: "竞争趋势 互联网大公司的寒冬要来了 各个巨头互联网..."
        },
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-006.png",
          title: "物联网",
          content: "+关注",
          de: "汽车在线报道最新路况信息 为您快速导航 避免拥..."
        },
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-007.png",
          title: "金融",
          content: "+关注",
          de: "竞争趋势 互联网大公司的寒冬要来了 各个巨头互联网..."
        },
        {
          img:
            "http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-008.png",
          title: "消费",
          content: "+关注",
          de: "汽车在线报道最新路况信息 为您快速导航 避免拥..."
        }
      ]
    };
  },
  methods: {
    getData(index) {
      this.activeIndex = index;
      if (index == 0) {
        console.log("查询专辑数据");
      } else {
        console.log("查询栏目的数据");
      }
    }
  }
};
</script>
<style lang="less" scoped>
.container {
  width: 100%;
  height: 800px;

  .ct-title {
    width: 100%;
    height: 50px;
    border: 1px solid white;
    border-bottom-color: #f0f0f0;
    margin-top: -90px;
    display: flex;
    flex-flow: row;
    align-items: center;
    justify-content: space-around;
    font-size: 16px;
    .ctname1 {
      color: #4285f4;
      width: 40px;
      height: 30px;
      border: 1px solid white;
      border-bottom-color: #4285f4;
      margin-top: 20px;
    }
    .ctname2 {
      color: #4285f4;
      width: 40px;
      height: 30px;
      border: 1px solid white;
      border-bottom-color: #4285f4;
      margin-top: 20px;
    }
  }
  .ct-body {
    width: 100%;
    height: 600px;

    margin-bottom: 49px;
    display: flex;
    flex-flow: row;
    flex-wrap: wrap;
    .ctb-container {
      position: relative;
      width: 155px;
      height: 150px;
      margin-left: 20px;
      margin-top: 10px;

      .ctb-img {
        // z-index: 1px;
        width: 155px;
        height: 100px;
        position: relative;
        .ctb {
          width: 155px;
          height: 100px;
          border: 1px solid white;
          border-radius: 6px;
        }
        .ctb-title {
          color: white;
          margin-top: -85px;
          font-size: 25px;
          font-family: "微软雅黑";
          display: flex;
          align-items: center;
          justify-content: center;
          background: aqua;
        }
      }
      .ctb-content {
        width: 120rpx;
        height: 60rpx;
        font-size: 15px;
        font-family: "微软雅黑";
        border: 2px solid white;
        border-radius: 18rpx;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: -40px;
        font-size: 13px;

        color: white;
        position: relative;
        z-index: 999;
        margin-left: 85rpx;
      }
      .ctb-de {
        margin-top: 15px;
        font-size: 12px;
        color: grey;
      }
    }
  }
}

.ct-new-tab {
  display: flex;
  width: 100%;
  margin-top: -180rpx;

  .tab-title {
    width: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 14x;
    border: 1px solid white;
    border-bottom-color: #f0f0f0;
    .tat {
      // background: aqua;
      // border: 1px solid white;
      // border-bottom-color: #4285f4;
    }
  }

  .tab-active {
    color: #4285f4;
    border: 1px solid white;
    border-bottom-color: #4285f4;
  }
}
</style>
