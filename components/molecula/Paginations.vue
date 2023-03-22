<template>
  <el-card>
    <div class="example-pagination-block">
      <div class="example-demonstration">When you have few pages</div>
      <el-pagination
        v-model:current-page="currentPagePaginations"
        :background="background"
        :hide-on-single-page="hide"
        layout="prev, pager, next"
        :total="totalPage"
        :disabled="disabled"
      />
    </div>
  </el-card>
</template>
<script lang="ts" setup>
import { computed } from 'vue';
const props = defineProps({
  background: {
    type: Boolean,
    default: true,
  },
  hide: {
    type: Boolean,
    default: false,
  },
  totalPage: {
    type: Number,
    default: 50,
  },
  disabled: {
    type: Boolean,
    default: false,
  },
  currentPage: {
    type: Number,
    default: 1,
  },
});
const currentPagePaginations = computed(() => {
  return props.currentPage;
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
