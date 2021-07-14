<template>
  <div class="editor" id="editor-layout-main">
    <a-layout :style="{background: '#fff'}">
      <a-layout-header>
        <div class="page-title">
          <img class="logo-img" src="https://opiece.com.cn/lego-img/logo2.cae6ad43.png" alt="Vue logo" />
        </div>
        <div class="right-col">
          <a-button type="primary" shape="round">登录</a-button>
        </div>
      </a-layout-header>
    </a-layout>
    <a-layout>
      <a-layout-sider width="300" style="background: yellow;">
        <div class="sidebar-container">
          组件列表
        </div>
      </a-layout-sider>
      <a-layout style="padding: 0 24px 24px;">
        <a-layout-content class="preview-container">
          <p>画布区域</p>
          <div class="preview-list" id="canvas-area">

          </div>
        </a-layout-content>
      </a-layout>
      <a-layout-sider width="300" style="background: purple" class="setting">
        组件属性
      </a-layout-sider>
    </a-layout>
    <a-layout>
      <a-layout-footer>
        &copy; 慕课网 (imooc.com) 版权所有 | 津ICP备20000929号
      </a-layout-footer>
    </a-layout>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
export default defineComponent({
  name: 'editor',

  methods: {}
})

</script>

<style scoped>
</style>
