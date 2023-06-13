
<template>
  <div class="logContainer">
    <el-card class="box-card">
      <div slot="header" class="clearfix">
        <a :href="github" target="_blank">
          <!-- <icon-svg icon-class="iconGithub" /> -->
        </a>

        <span>项目更新日志：</span>
        <!-- <span>项目简介：</span> -->
      </div>
      <!-- <span>小爱为一个投资管理系统,该系统有管理者和用户两个系统，管理者可以对用户进行管理，用户可以登录使用资金管理，资金数据，投资管理，数据分析等功能。</span> -->
      <div class="logArea el-scrollbar">
        <div class="item" v-for="(item,index) in logsData" :key="index">
          <p class="timeArea">
            <span class="title">日期：</span>
            <span class="title time">{{item.createTime}}</span>
            <!-- <span class="title time">2022-09-08</span> -->
          </p>
          <div class="logContent">
            <p class="title">更新内容：</p>
            <ul class="logUl">
              <li v-for="(citem,cindex) in item.data" :key="cindex">{{citem}}</li>
            </ul>
          </div>
        </div>
      </div>

    </el-card>
  </div>
</template>

<script>
import logsData from '@/assets/datas/logs.json'
import { github } from '@/utils/env'

export default {
  name: 'logList',
  data() {
    return {
      logsData: logsData.data,
      github: github
    }
  }
}
</script>

<style lang="less" scoped>
.logContainer {
  padding: 10px;
  background: #fff;
  box-sizing: border-box;
  height: 370px;
  max-height: 370px;
  overflow: hidden;
  border-radius: 6px;
  .logArea {
    overflow: auto;
    height: 100%;
  }
  .item {
    .title {
      font-size: 13px;
    }
    .time {
      color: #87de75;
    }
    .logContent {
      .logUl {
        padding-left: 30px;
        li {
          font-size: 12px;
          list-style: disc;
          line-height: 20px;
        }
      }
    }
  }
}
.clearfix:before,
.clearfix:after {
  display: table;
  content: '';
}

.clearfix:after {
  clear: both;
}
</style>

