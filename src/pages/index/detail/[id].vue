<script setup>
import { useRoute } from 'vue-router'

const data = {
  report_info: {
    repair_id: '3',
    updated_at: '1688348336',
    created_at: '1688348336',
    comment: '条明构那入更家内地点图子人北列大。',
    score: '5.36039',
    result: '半委解化社装手加根做矿至价然效参式例。明北导所克飞水员进院步育空相适准。至主程象很边众矿合达深水利完已你层动。',
    finish_time: '1688348336',
    address: '从解出品太即至强劳之因干原上。',
    request_time: '1688348336',
    is_urgent: 'false',
    worker_id: '4',
    admin_id: '5',
    user_id: '6',
    detail: '局石易增细军力但据格民教场。',
    type: '玻璃类',
    assign_time: '1688348336',
    status: '待核验',
    id: '7',
    account: 'Larry',
    name: '韩杰',
    sex: '女',
    phone: '18191821238',
    department: '己',
    role: 'admin',
  },
  actual_info: 'cillum ut in',
  estimate_info: 'dolore sint dolore',
  assign_info: {
    '': 'cupidatat ipsum aliquip',
  },
  comment_info: 'officia exercitation Ut sunt ea',
  status: 'esse laboris cillum ea sunt',
  created_at: '2015-01-13 07:41:26',
  updated_at: '2020-04-29 13:30:05',
}
const label = [
  {
    label: '报修项目',
    value: 'type',
  },
  {
    label: '报修地址',
    value: 'address',
  },
  {
    label: '报修详情',
    value: 'detail',
  },
  {
    label: '是否紧急',
    value: 'is_urgent',
  },
  {
    label: '报修人',
    value: 'user_id',
  },
  {
    label: '报修时间',
    value: 'request_time',
  },
  {
    label: '维修状态',
    value: 'status',
  },
  {
    label: '维修单号',
    value: 'id',
  },
  {
    label: '报修人账号',
    value: 'account',
  },
  {
    label: '报修人姓名',
    value: 'name',
  },
  {
    label: '报修人性别',
    value: 'sex',
  },
  {
    label: '报修人电话',
    value: 'phone',
  },
  {
    label: '报修人部门',
    value: 'department',
  },
  {
    label: '维修单号',
    value: 'repair_id',
  },
  {
    label: '更新时间',
    value: 'updated_at',
  },
  {
    label: '创建时间',
    value: 'created_at',
  },
  {
    label: '维修评分',
    value: 'score',
  },
  {
    label: '维修结果',
    value: 'result',
  },
  {
    label: '完成时间',
    value: 'finish_time',
  },
  {
    label: '维修人员ID',
    value: 'worker_id',
  },
  {
    label: '管理员ID',
    value: 'admin_id',
  },
]

function get_status() {
  judgment_status = data.report_info.status
  return judgment_status
}

const res = label.map((element) => {
  return {
    label: element.label,
    value: data.report_info[element.value],
  }
})
const id = useRoute().params.id
</script>

<template>
  {{ id }}
  <a-space direction="vertical" size="large" class="px-2">
    <a-card>
      <a-descriptions :data="res" :title="data.report_info.status" layout="inline-vertical" table-layout="auto" />
    </a-card>
  </a-space>
</template>

<style>
.arco-descriptions-title {
  @apply text-[16px];
}

.arco-descriptions {
  @apply px-[20px];
}
</style>
