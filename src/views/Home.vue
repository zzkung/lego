<template>
  <div class="homepage-container">
    <a-layout :style="{background: '#fff'}">
      <a-layout-header class="header transparent-header">
        <div class="page-title">
          <img class="logo-img" src="https://opiece.com.cn/lego-img/logo2.cae6ad43.png" alt="Vue logo" />
        </div>
        <div class="right-col">
          <a-button type="primary" shape="round">登录</a-button>
        </div>
      </a-layout-header>
      <a-layout-content class="home-layout">
        <div class="homepage-container">
          <div class="banner">
            <a-image class="banner-img" width="100%" height="100%" src="https://opiece.com.cn/lego-img/background.3744875e.png" :preview="false" />
            <div class="banner-text">
              <h2 class="text-headline">海量精彩设计 一键生成</h2>
              <a-input-search
                v-model:value="value"
                placeholder="搜索一下，快速找模板"
                enter-button
                @search="onSearch"
              />
            </div>
          </div>
          <div class="content-container">
            <template-list :list="testData"></template-list>
          </div>
        </div>
      </a-layout-content>
      <a-layout-footer>
        &copy; 慕课网 (imooc.com) 版权所有 | 津ICP备20000929号
      </a-layout-footer>
    </a-layout>
  </div>
</template>

<script>
import TemplateList from '@/components/TemplateList.vue'
export default {
  name: 'home',
  components: {
    TemplateList
  },
  data () {
    return {
      value: '',
      testData: [
        {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-889755.png',
          title: '前端架构师直播海报',
          author: 'Viking张轩',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-977815.png',
          title: '1024 程序员日',
          author: 'Miss.Lu',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-323204.png',
          title: '招聘-慕课乐高',
          author: 'Miss.Lu',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-677311.png',
          title: '未命名作品',
          author: 'Viking张轩',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-133701.png',
          title: '慕课 Live Java 入门编程课',
          author: 'Viking张轩',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-726751.png',
          title: '慕课资讯',
          author: 'Viking张轩',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-682056.png',
          title: '每日分享',
          author: 'Viking张轩',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-649919.png',
          title: '慕课 Live',
          author: 'Viking张轩',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-882241.png',
          title: '幸福的方法',
          author: '双越',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-126349.png',
          title: '樊登读书-意志力',
          author: '双越',
          userNum: 664
        }, {
          coverImg: 'https://opiece.com.cn/lego-img/screenshot-388804.png',
          title: '中秋快乐',
          author: '双越',
          userNum: 664
        }
      ]
    }
  },

  methods: {
    onSearch(value, event) {
      console.log(value, event)
    }
  }
}

</script>

<style scoped>
.content-container {
  background: #fff;
  padding: 30px 24px;
  min-height: 85vh;
  max-width: 1200px;
  margin: 0 auto;
  width: 100%;
}
</style>
