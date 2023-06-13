<template>
  <div class='footer'>
    <!-- <p class="intro rflex">
      <span>{{ $t('commons.xiaoai') }}.AiT</span> -->
    <!-- <a :href='github' target="_blank">
        <icon-svg icon-class="iconGithub" />
      </a> -->
    <!-- <span>AiTou2022({{ $t('commons.wechatNumber') }})</span> -->
    <!-- <icon-svg icon-class="iconGithub" /> -->
    <!-- 
    </p> -->
    <p>{{ $t('commons.xiaoai') }}.AiT</p>
    <span>地址:河南开封龙亭</span>
    <p class="beian">豫ICP备180016123号</p>
  </div>
</template>


<script>
import { github } from '@/utils/env'

export default {
  name: 'footerNav',
  data() {
    return {
      github: github
    }
  },
  methods: {}
}
</script>

<style lang="less">
.footer {
  width: 100%;
  padding: 10px 0;
  font-size: 12px;
  text-align: center;
  background: #fff;
  p {
    line-height: 30px;
  }
  .intro {
    width: 240px;
    margin: 0 auto;
    justify-content: space-between;
    align-items: center;
  }
}
</style>


 