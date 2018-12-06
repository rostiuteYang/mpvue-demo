<template>
  <div class="container">
    <div class="ct-title">
      <div class="ct-name1">专辑</div>
      <div class="ct-name2">栏目</div>
    </div>
    <div class="ct-body">
      <div class="ctb-container">
        <div class="ctb-img">
          <img
            src="http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-001.png"
            class="ctb"
          >
          <div class="ctb-title">大公司</div>
        </div>
        <button class="ctb-content">+关注</button>
        <div class="ctb-de">竞争趋势 互联网大公司的寒冬要来了 各个巨头互联网...</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style lang="less" scoped>
.container {
  width: 100%;
  height: 800px;

  .ct-title {
    width: 100%;
    height: 50px;

    margin-top: -90px;
    display: flex;
    flex-flow: row;
    align-items: center;
    justify-content: space-around;
    font-size: 16px;
  }
  .ct-body {
    width: 100%;
    height: 600px;

    margin-bottom: 49px;
    display: flex;
    flex-flow: row;
    flex-wrap: wrap;
    .ctb-container {
      width: 155px;
      height: 150px;
      // background: aqua;
      margin-left: 20px;
      margin-top: 20px;
      .ctb-img {
        width: 155px;
        height: 100px;
        .ctb {
          width: 155px;
          height: 100px;
          border: 1px solid white;
          border-radius: 6px;
        }
        .ctb-title {
          color: white;
          font-size: 20px;
          margin-left: 40px;
          margin-top: -85px;
          font-size: 25px;
          font-family: "微软雅黑";
        }
      }
      .ctb-content {
        // background: rgb(0, 0, 0.5);
        width: 80px;
        height: 35px;
        color: white;
        font-size: 15px;
        font-family: "微软雅黑";
        border: 2px solid white;
        border-radius: 18px;
        margin-left: 40px;
        margin-top: -40px;
        font-size: 13px;
        background-image: url(http://www.17sucai.com/preview/1268063/2018-12-04/attend/images/icon-att-001.png);
      }
      .ctb-de {
        margin-top: 5px;
        font-size: 14px;
        color: grey;
      }
    }
  }
}
</style>
