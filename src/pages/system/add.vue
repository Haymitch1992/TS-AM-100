<template>
  <a-card :body-style="{ padding: '24px 32px' }" :bordered="false">
    <a-form>
      <a-form-item
        label="子系统名称"
        :labelCol="{ span: 7 }"
        :wrapperCol="{ span: 10 }"
      >
        <a-input placeholder="请输入子系统名称" />
      </a-form-item>
      <a-form-item
        label="子系统路由"
        :labelCol="{ span: 7 }"
        :wrapperCol="{ span: 10 }"
      >
        <a-input placeholder="请输入子系统路由" />
      </a-form-item>
      <a-form-item
        label="系统负责人"
        :labelCol="{ span: 7 }"
        :wrapperCol="{ span: 10 }"
      >
        <a-input placeholder="例如：付哲" />
      </a-form-item>
      <a-form-item
        label="团队成员(选填)"
        :labelCol="{ span: 7 }"
        :wrapperCol="{ span: 10 }"
        :required="false"
      >
        <a-input-number :min="0" :max="100" />
        <span>人</span>
      </a-form-item>
      <a-form-item
        label="产品描述"
        :labelCol="{ span: 7 }"
        :wrapperCol="{ span: 10 }"
      >
        <a-textarea
          rows="4"
          placeholder="面向智慧城轨业务体系，提供通用化、高指标AI算法"
        />
      </a-form-item>
      <a-form-item
        label="版本号"
        :labelCol="{ span: 7 }"
        :wrapperCol="{ span: 10 }"
      >
        <a-input placeholder="V1.0.0" />
      </a-form-item>
      <a-form-item
        label="是否公开"
        :labelCol="{ span: 7 }"
        :wrapperCol="{ span: 10 }"
        :required="false"
      >
        <a-radio-group v-model="value">
          <a-radio :value="1">公开</a-radio>
          <a-radio :value="2">私有</a-radio>
        </a-radio-group>
      </a-form-item>
      <a-form-item
        style="margin-top: 24px"
        :wrapperCol="{ span: 10, offset: 7 }"
      >
        <a-button type="primary" @click="submitForm()">提交</a-button>
        <a-button style="margin-left: 8px">取消</a-button>
      </a-form-item>
    </a-form>
  </a-card>
</template>

<script>
export default {
  name: 'BasicForm',
  data() {
    return {
      value: 1,
      desc: '交控科技旗下的人工智能平台，提供一站式的机器学习解决方案。',
      extraImage:
        'https://gw.alipayobjects.com/zos/rmsportal/RzwpdLnhmvDJToTdfDPe.png',
    };
  },
  methods: {
    submitForm() {
      this.$router.push('/system/list');
    },
  },
};
</script>

<style scoped></style>
