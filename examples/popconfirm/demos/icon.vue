<template>
  <div class="popconfirm-demo">
    <div class="tdesign-demo-block">
      <div class="demo-item">
        <t-popconfirm content="普通事件通知类型偏向于确认" v-model="visible1">
          <t-button>默认</t-button>
        </t-popconfirm>
      </div>

      <div class="demo-item">
        <t-popconfirm theme="warning" content="事件通知类型偏向于提示" v-model="visible2">
          <t-button theme="warning">警告</t-button>
        </t-popconfirm>
      </div>

      <div class="demo-item">
        <t-popconfirm theme="danger" content="事件通知类型偏向于高危提醒" v-model="visible3">
          <t-button theme="danger">危险</t-button>
        </t-popconfirm>
      </div>
    </div>

    <br><br>
    <div class="tdesign-demo-block">
      <div class="demo-item">
        <t-popconfirm content="基础气泡确认框文案示意文字按钮" :popupProps="{ placement: 'bottom' }">
          <icon name="browse" style="color: #0052d9" slot='icon'/>
          <t-button variant="outline">自定义图标（插槽）</t-button>
        </t-popconfirm>
      </div>

      <div class="demo-item">
        <t-popconfirm content="基础气泡确认框文案示意文字按钮" :icon='customIcon' :popupProps="{ placement: 'bottom' }">
          <t-button variant="outline">自定义图标（属性）</t-button>
        </t-popconfirm>
      </div>
    </div>
  </div>
</template>

<script lang="jsx">
import { Icon } from 'tdesign-icons-vue';

export default {
  components: {
    Icon,
  },
  data() {
    return {
      visible1: true,
      visible2: false,
      visible3: false,
    };
  },
  methods: {
    customIcon() {
      return (<Icon name='browse' style="margin-right: 8px"/>);
    },
  },
};
</script>

<style scoped>
.popconfirm-demo .tdesign-demo-block {
  display: flex;
  justify-content: flex-start;
}
.popconfirm-demo .demo-item {
  width: 240px;
  text-align: left;
}
</style>
