<template>
  <div>
    <t-cascader
      v-model="value"
      :options="options"
      clearable
      size="medium"
      placeholder='请选择'
      class="t-demo-cascader"
      @change="onChange"
    ></t-cascader>
  </div>
</template>

<script>
export default {
  data() {
    return {
      options: [
        {
          label: '选项一',
          value: '1',
          children: [
            {
              label: '子选项一',
              value: '1.1',
            },
            {
              label: '子选项二',
              value: '1.2',
            },
            {
              label: '子选项三',
              value: '1.3',
            },
          ],
        },
        {
          label: '选项二',
          value: '2',
          children: [
            {
              label: '子选项一',
              value: '2.1',
            },
            {
              label: '子选项二',
              value: '2.2',
            },
          ],
        },
      ],
      value: '1.1',
    };
  },
  methods: {
    onChange(val, context) {
      console.log(this.value, val, context);
      console.log('path: ', context.node.getPath());
    },
  },
};
</script>
<style scoped>
.t-demo-cascader-title {
  margin: 10px 0;
}
.t-demo-cascader + .t-demo-cascader {
  margin-top: 16px;
}
</style>
