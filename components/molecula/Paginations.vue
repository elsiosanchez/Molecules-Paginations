<template>
  <el-card>
    <div class="example-pagination-block">
      <div class="example-demonstration">When you have few pages</div>
      <el-pagination layout="prev, pager, next" :total="50" />
    </div>
    <div class="example-pagination-block">
      <div class="example-demonstration">When you have more than 7 pages</div>
      <el-pagination layout="prev, pager, next" :total="1000" />
    </div>
  </el-card>
</template>
<script lang="ts" setup>
const props = defineProps({
  showClear: {
    type: Boolean,
    required: true,
  },
  showClose: {
    type: Boolean,
    required: true,
  },
  showCheck: {
    type: Boolean,
    required: true,
  },
  actionClear: {
    type: Function,
    default: (clean) => {
      console.info('Implement the Clean Method', clean);
    },
  },
  actionClose: {
    type: Function,
    default: (close) => {
      console.info('Implement the Close Method', close);
    },
  },
  actionCheck: {
    type: Function,
    default: (check) => {
      console.info('Implement the Check Method', check);
    },
  },
  disabledClear: {
    type: Boolean,
    default: false,
  },
  disabledClose: {
    type: Boolean,
    default: false,
  },
  disabledCheck: {
    type: Boolean,
    default: false,
  },
  textAling: {
    type: String,
    required: false,
    default: 'Right',
  },
  slotsLeft: String,
  slotsRight: String,
  slotsAlingLeft: String,
  slotsAlingRight: String,
});
</script>

<style scoped>
.example-pagination-block + .example-pagination-block {
  margin-top: 10px;
}
.example-pagination-block .example-demonstration {
  margin-bottom: 16px;
}
</style>
