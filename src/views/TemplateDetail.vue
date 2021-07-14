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
      <a-layout-content>
        <div class="work-detail-container">
          <a-row :gutter="30" justify="center">
            <a-col :span="8" class="cover-img">
              <a-image width="100%" src="https://opiece.com.cn/lego-img/screenshot-726751.png" alt="" />
            </a-col>
            <a-col :span="8">
              <h2>前端架构师直播海报</h2>
              <p>未命名作品</p>
              <div class="author">
                <a-avatar shape="circle" src="" :style="{marginRight: '10px'}">
                  <template #icon><UserOutlined /></template>
                </a-avatar>
                该模板由 <b>Viking张轩</b> 创作
              </div>
              <div class="bar-code-area">
                <span>扫一扫，手机预览</span>
                <div title="https://h5.imooc-lego.com/p/7-339e"></div>
              </div>
              <div class="use-button">
                <a-button type="primary" shape="round">使用模板</a-button>
                <a-button shape="round" :style="{marginLeft: '20px'}">下载图片海报</a-button>
              </div>
            </a-col>
          </a-row>
        </div>
      </a-layout-content>
      <a-layout-footer>
        &copy; 慕课网 (imooc.com) 版权所有 | 津ICP备20000929号
      </a-layout-footer>
    </a-layout>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
import { UserOutlined } from '@ant-design/icons-vue'
export default defineComponent({
  name: 'templateDetail',
  components: {
    UserOutlined,
  },

  methods: {}
})

</script>

<style scoped>
.work-detail-container {
  padding: 0 24px;
  min-height: 85vh;
  min-width: 800px;
  max-width: 1200px;
  margin: 138px auto 74px;
  width: 100%;
}
.bar-code-area {
  margin: 20px 0;
}
.use-button {
  margin: 30px 0;
}
</style>
