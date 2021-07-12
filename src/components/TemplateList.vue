<template>
  <div class="template-list-component">
    <a-row :gutter="16">
      <a-col :span="6" v-for="item in list" :key="item" class="poster-item">
        <a-card hoverable>
          <template #cover>
            <img :src="item.coverImg" v-if="item.coverImg" />
            <img src="" v-else />
            <div class="hover-item">
              <a-button size="large" type="primary" shape="round">使用该模板创建</a-button>
            </div>
          </template>
          <a-card-meta :title="item.title">
            <template #description>
              <div class="description-detail">
                <span>作者：{{item.author}}</span>
                <span class="user-number"><UserOutlined />{{item.userNum}}</span>
              </div>
            </template>
          </a-card-meta>
        </a-card>
      </a-col>
    </a-row>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { UserOutlined } from '@ant-design/icons-vue'
export default defineComponent({
  name: 'template-list',
  components: { UserOutlined },
  props: {
    list: {
      type: Array,
      required: true
    },
    type: {
      type: String,
      default: 'work'
    }
  }
})

</script>

<style>
.poster-item {
  position: relative;
  margin-bottom: 20px;
}
.poster-item .ant-card-hoverable {
  box-shadow: 0 5px 10px 0 rgb(0 0 0 / 10%);
}
.poster-item .ant-card {
  border-radius: 12px;
}
.poster-item .ant-card-cover {
  position: relative;
  overflow: hidden;
  border-top-left-radius: 12px;
  border-top-right-radius: 12px;
}
.poster-item .ant-card-cover {
  height: 390px;
}
.poster-item .ant-card-cover img {
  transition: all .2s ease-in;
}
.poster-item .ant-card-cover>img {
  width: 100%;
}
.hover-item {
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  display: none;
  background: rgba(0,0,0,.8);
  align-items: center;
  justify-content: center;
  border-top-left-radius: 12px;
  border-top-right-radius: 12px;
}
.poster-item:hover .hover-item {
	display: flex;
}
.poster-item:hover img {
	transform: scale(1.25);
}
.poster-item .ant-card-body {
  padding: 0;
}
.poster-item .ant-card-meta {
  margin: 0;
}
.poster-item .ant-card-meta-title {
  color: #333;
  padding: 10px 12px;
  border-bottom: 1px solid #f2f2f2;
  margin-bottom: 0!important;
}
.description-detail {
  display: flex;
  justify-content: space-between;
  padding: 13px 12px;
  color: #999;
}
.user-number {
  font-weight: 700;
}
</style>
