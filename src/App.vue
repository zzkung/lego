<template>
  <!-- <home /> -->
  <editor />
  <!-- <template-detail /> -->
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Home from './views/Home.vue'
import TemplateDetail from './views/TemplateDetail.vue'
import Editor from './views/Editor.vue'
export default defineComponent({
  name: 'App',
  components: {
    // Home,
    Editor,
    // TemplateDetail
  }
})
</script>

<style>
.transparent-header {
  background-color: rgba(0, 0, 0, .5);
}
.ant-layout-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  z-index: 50;
  box-shadow: 0 10px 15px rgb(0, 0, 0 / 10%);
}
.header {
  position: fixed;
  width: 100%;
}
.logo-img {
  height: 35px;
}
.right-col {
  margin-left: 30px;
}
.banner {
  display: flex;
  position: relative;
  height: 450px;
  width: 100%;
  overflow: hidden;
}
.banner img {
  object-fit: cover;
}
.banner-text {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  box-sizing: border-box;
}
.text-headline {
  text-shadow: 0 0 1px rgb(68, 92, 116 / 2%);
  font-size: 2em;
  color: #fff;
}
.banner-text .ant-input-search {
  width: 40%;
  box-shadow: 0 12px 24px 0 rgb(30 29 32 / 80%);
  border-radius: 20px;
}
.banner-text .ant-input {
  height: 40px;
  font-size: 17px;
  padding: 7px 15px;
  padding-right: 30px;
  border: 2px solid #1890ff;
  border-right-width: 0;
  border-radius: 20px;
}
.banner-text .ant-input-group-addon {
  border-radius: 20px;
}
.banner-text .ant-input-search-button {
  height: 40px;
  border: 2px solid #1890ff;
  border-left-width: 0;
  border-radius: 20px;
  display: flex;
  align-items: center;
}
.banner-text .ant-input-search-button svg {
  font-size: 25px;
}
</style>
