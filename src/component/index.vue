<template>
    <div class='wrap'>
        <header class='header'>
            <div class="head wraper">
                <img src="../img/logo.png" alt="">
                <ul>
                    <li>产品</li>
                    <li>关于我们</li>
                    <li>大数据</li>
                    <li>新闻</li>
                    <li>招聘</li>
                    <li>商城</li>
                    <li>登录/注册</li>
                </ul>
                <i class="icon"><img src="../img/列表.png" alt=""></i>
            </div>
        </header>
        <div class="banner">
            <img src="../img/banner.png" alt="">
        </div> 
        <div class="tap">
            <div class="taplist wraper">
                <ul>
                    <li>分析评论</li>
                    <li>趋势榜单</li>
                    <li>研究报告</li>
                </ul>
            </div>
        </div>
         <div class="section">
            <div class="con wraper">
                <div class="one">
                    <h3><i></i><span>SUV</span><em>TOP10</em></h3>
                    <div id="myChart" :style="{width: '800px', height: '400px'}"></div>
                </div>
                <div class='list'>
                    <p>竞购胜率排行榜</p>
                    <ul>
                        <li><b>1</b><em>汉兰达</em><span>66.9%</span></li>
                        <li><b>2</b><em>汉兰达</em><span>66.9%</span></li>
                        <li><b>3</b><em>汉兰达</em><span>66.9%</span></li>
                        <li><b>4</b><em>汉兰达</em><span>66.9%</span></li>
                        <li><b>5</b><em>汉兰达</em><span>66.9%</span></li>
                        <li><b>6</b><em>汉兰达</em><span>66.9%</span></li>
                        <li><b>7</b><em>汉兰达</em><span>66.9%</span></li>
                    </ul>
                </div>
                 <div class="one">
                    <h3><i></i><span>SUV</span><em>TOP10</em></h3>
                    <div id="myChart1" :style="{width: '800px', height: '400px'}"></div>
                </div>
                <div class="one">
                    <h3><i></i><span>SUV</span><em>TOP10</em></h3>
                    <div id="myChart2" :style="{width: '800px', height: '400px'}"></div>
                </div>
            </div>
        </div>
    </div>
     
        
</template>
<script>
import '../flexible'
export default {
    name:'index',
    mounted() {
        this.draw()
    },
   methods: {
    draw(){
        // 基于准备好的dom，初始化echarts实例
        let myChart = this.$echarts.init(document.getElementById('myChart'))
        let myChart1 = this.$echarts.init(document.getElementById('myChart1'))
        let myChart2 = this.$echarts.init(document.getElementById('myChart2'))
        // 绘制图表
        myChart.setOption({
          tooltip: {
              trigger: 'axis'
          },
          legend: {
              data:['吉利博越','冠道','本田XR-V','哈弗H6','途观','全新途胜','本田CR-V','缤智','奔驰GLA级','汉兰达']
          },
          grid: {
              left: '3%',
              right: '4%',
              bottom: '3%',
              containLabel: true
          },
          toolbox: {
              feature: {
                  saveAsImage: {}
              }
          },
          xAxis: {
              type: 'category',
              boundaryGap: false,
              data: ['Jan/18','Mar/18','May/18','Jul/18','Sep/18','Nov/18']
          },
          yAxis: {
              type: 'value'
          },
          series: [
              {
                  name:'吉利博越',
                  type:'line',
                  stack: '总量',
                  data:[120, 132, 101, 134, 100, 230]
              },
              {
                  name:'冠道',
                  type:'line',
                  stack: '总量',
                  data:[120, 182, 191, 334, 290, 330]
              },
              {
                  name:'本田XR-V',
                  type:'line',
                  stack: '总量',
                  data:[150, 232, 401, 154, 190, 330]
              },
              {
                  name:'哈弗H6',
                  type:'line',
                  stack: '总量',
                  data:[320, 332, 301, 334, 390, 330]
              },
              {
                  name:'全新途胜',
                  type:'line',
                  stack: '总量',
                  data:[820, 932, 901, 934, 1290, 1330]
              },
              {
                  name:'本田CR-V',
                  type:'line',
                  stack: '总量',
                  data:[200, 300, 400, 500, 600, 700]
              },
              {
                  name:'缤智',
                  type:'line',
                  stack: '总量',
                  data:[123, 444, 785, 456, 789, 700]
              },
              {
                  name:'奔驰GLA级',
                  type:'line',
                  stack: '总量',
                  data:[155, 489, 357, 753, 851, 951]
              },
              {
                  name:'汉兰达',
                  type:'line',
                  stack: '总量',
                  data:[555, 666, 888, 772, 687, 786]
              }
          ]
        });
         myChart1.setOption({
          tooltip: {
              trigger: 'axis'
          },
          legend: {
              data:['吉利博越','冠道','本田XR-V','哈弗H6','途观','全新途胜','本田CR-V','缤智','奔驰GLA级','汉兰达']
          },
          grid: {
              left: '3%',
              right: '4%',
              bottom: '3%',
              containLabel: true
          },
          toolbox: {
              feature: {
                  saveAsImage: {}
              }
          },
          xAxis: {
              type: 'category',
              boundaryGap: false,
              data: ['Jan/18','Mar/18','May/18','Jul/18','Sep/18','Nov/18']
          },
          yAxis: {
              type: 'value'
          },
          series: [
              {
                  name:'吉利博越',
                  type:'line',
                  stack: '总量',
                  data:[120, 132, 101, 134, 100, 230]
              },
              {
                  name:'冠道',
                  type:'line',
                  stack: '总量',
                  data:[120, 182, 191, 334, 290, 330]
              },
              {
                  name:'本田XR-V',
                  type:'line',
                  stack: '总量',
                  data:[150, 232, 401, 154, 190, 330]
              },
              {
                  name:'哈弗H6',
                  type:'line',
                  stack: '总量',
                  data:[320, 332, 301, 334, 390, 330]
              },
              {
                  name:'全新途胜',
                  type:'line',
                  stack: '总量',
                  data:[820, 932, 901, 934, 1290, 1330]
              },
              {
                  name:'本田CR-V',
                  type:'line',
                  stack: '总量',
                  data:[200, 300, 400, 500, 600, 700]
              },
              {
                  name:'缤智',
                  type:'line',
                  stack: '总量',
                  data:[123, 444, 785, 456, 789, 700]
              },
              {
                  name:'奔驰GLA级',
                  type:'line',
                  stack: '总量',
                  data:[155, 489, 357, 753, 851, 951]
              },
              {
                  name:'汉兰达',
                  type:'line',
                  stack: '总量',
                  data:[555, 666, 888, 772, 687, 786]
              }
          ]
        });
        myChart2.setOption({
          tooltip: {
              trigger: 'axis'
          },
          legend: {
              data:['吉利博越','冠道','本田XR-V','哈弗H6','途观','全新途胜','本田CR-V','缤智','奔驰GLA级','汉兰达']
          },
          grid: {
              left: '3%',
              right: '4%',
              bottom: '3%',
              containLabel: true
          },
          toolbox: {
              feature: {
                  saveAsImage: {}
              }
          },
          xAxis: {
              type: 'category',
              boundaryGap: false,
              data: ['Jan/18','Mar/18','May/18','Jul/18','Sep/18','Nov/18']
          },
          yAxis: {
              type: 'value'
          },
          series: [
              {
                  name:'吉利博越',
                  type:'line',
                  stack: '总量',
                  data:[120, 132, 101, 134, 100, 230]
              },
              {
                  name:'冠道',
                  type:'line',
                  stack: '总量',
                  data:[120, 182, 191, 334, 290, 330]
              },
              {
                  name:'本田XR-V',
                  type:'line',
                  stack: '总量',
                  data:[150, 232, 401, 154, 190, 330]
              },
              {
                  name:'哈弗H6',
                  type:'line',
                  stack: '总量',
                  data:[320, 332, 301, 334, 390, 330]
              },
              {
                  name:'全新途胜',
                  type:'line',
                  stack: '总量',
                  data:[820, 932, 901, 934, 1290, 1330]
              },
              {
                  name:'本田CR-V',
                  type:'line',
                  stack: '总量',
                  data:[200, 300, 400, 500, 600, 700]
              },
              {
                  name:'缤智',
                  type:'line',
                  stack: '总量',
                  data:[123, 444, 785, 456, 789, 700]
              },
              {
                  name:'奔驰GLA级',
                  type:'line',
                  stack: '总量',
                  data:[155, 489, 357, 753, 851, 951]
              },
              {
                  name:'汉兰达',
                  type:'line',
                  stack: '总量',
                  data:[555, 666, 888, 772, 687, 786]
              }
          ]
        });
    }
  }
}
</script>
<style lang="">
    @import "../css/home.css";
</style>