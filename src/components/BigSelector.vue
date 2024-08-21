<template>
  <h2 style="text-align: center">项目收费选择器</h2>

  <div style="margin: 20px">
    <el-button style="" type="primary">保存</el-button>

    <el-button>打印尸检书</el-button>
    <el-button>打印辨认遗体通知单</el-button>
  </div>

  <div style="margin: 20px; display: flex; flex-direction: row; gap: 10px">
    <div style="display: flex; flex-direction: column; gap: 10px; width: 240px">
      <div style="display: flex; gap: 10px">
        <el-input
          style="width: 200px"
          placeholder="搜索"
          :prefix-icon="Search"
        />
      </div>
      <el-table :data="tableData" border>
        <el-table-column prop="date" label="服务项目类型" />
      </el-table>
    </div>

    <div style="display: flex; flex-direction: column; gap: 10px">
      <div style="display: flex; gap: 10px">
        <el-button style="" type="primary">添加 </el-button>
        <el-input
          style="width: 200px"
          placeholder="搜索"
          :prefix-icon="Search"
        />
      </div>
      <el-table
        :data="data2"
        border
        style="width: auto; max-height: 800px; overflow-y: auto"
      >
        <el-table-column type="selection" width="50" />
        <el-table-column prop="prop2" label="服务项目" width="180" />
        <el-table-column prop="prop3" label="单位" width="100" />
        <el-table-column prop="prop4" label="单价" width="100" />
        <el-table-column label="数量" width="150">
          <el-input-number
            :modelValue="1"
            class="input-number"
            :min="1"
            :max="10"
          />
        </el-table-column>
      </el-table>
    </div>
    <el-button type="primary" style="align-self: center">></el-button>
    <div style="display: flex; flex-direction: column; gap: 10px">
      <div style="display: flex; gap: 10px">
        <el-button style="" type="danger" disabled>删除 </el-button>
        <el-input
          style="width: 200px"
          placeholder="搜索"
          :prefix-icon="Search"
        />
      </div>
      <el-table :data="data3" border style="width: auto">
        <el-table-column type="selection" width="50" />
        <el-table-column prop="prop2" label="服务项目" width="180" />
        <el-table-column prop="prop3" label="单位" width="100" />
        <el-table-column prop="prop4" label="单价" width="100" />
        <el-table-column label="数量" width="150">
          <el-input-number
            :modelValue="1"
            class="input-number"
            :min="1"
            :max="10"
        /></el-table-column>
        <el-table-column prop="prop4" label="金额" width="100" />
        <el-table-column prop="prop4" label="应收金额" width="100" />
        <el-table-column label="操作" width="100">
          <div style="display: flex; align-items: center; gap: 10px">
            <el-button type="danger" size="small" :icon="Delete" />
          </div>
        </el-table-column>
      </el-table>
    </div>
  </div>
</template>

<script lang="ts" setup>
import { Delete, Search } from "@element-plus/icons-vue";

const tableData = [
  {
    date: "预设组合1",
  },
  {
    date: "预设组合2",
  },
  {
    date: "遗体火化基本服务",
  },
  {
    date: "棺木",
  },
  {
    date: "骨灰盅",
  },
  {
    date: "骨灰箱",
  },
  {
    date: "骨灰塔",
  },
  {
    date: "冷藏",
  },
  {
    date: "特需服务",
  },
  {
    date: "告别厅服务",
  },
  {
    date: "鲜花",
  },
  {
    date: "被子枕头",
  },
];
const data2 = [
  { prop2: "遗体运送", prop3: "具", prop4: "180" },
  { prop2: "消毒", prop3: "具", prop4: "100" },
  { prop2: "包裹", prop3: "具", prop4: "100" },
  { prop2: "专车收殓遗体", prop3: "具", prop4: "100" },
  { prop2: "遗物焚化", prop3: "袋", prop4: "50" },
  { prop2: "拣灰炉", prop3: "具", prop4: "850" },
  { prop2: "化妆1", prop3: "宗", prop4: "150" },
  { prop2: "遗体清洗", prop3: "具", prop4: "200" },
  { prop2: "遗体穿、脱衣", prop3: "具", prop4: "200" },
  { prop2: "铺衣服", prop3: "具", prop4: "200" },
  { prop2: "租用休息室", prop3: "2小时/间", prop4: "400" },
  { prop2: "租用休息室", prop3: "小时/间", prop4: "200" },
  { prop2: "观化室礼仪服务", prop3: "宗", prop4: "80" },
  { prop2: "带棺火化B", prop3: "副", prop4: "380", disabled: true },
  { prop2: "带棺火化C", prop3: "副", prop4: "260", disabled: true },
  { prop2: "带棺火化D", prop3: "副", prop4: "240", disabled: true },
  { prop2: "带棺火化E", prop3: "副", prop4: "80", disabled: true },
  { prop2: "骨灰处理", prop3: "份", prop4: "50" },
  { prop2: "跨市县遗体接运", prop3: "公里", prop4: "3.5" },
  { prop2: "遗体火化", prop3: "具", prop4: "230" },
  { prop2: "出租拜祭房", prop3: "场", prop4: "480" },
  { prop2: "二次消毒", prop3: "具", prop4: "100" },
];
const data3 = [
  { prop2: "遗体运送", prop3: "具", prop4: "180" },
  { prop2: "消毒", prop3: "具", prop4: "100" },
  { prop2: "专车收殓遗体", prop3: "具", prop4: "100" },
  { prop2: "遗物焚化", prop3: "袋", prop4: "50" },
  { prop2: "拣灰炉", prop3: "具", prop4: "850" },
  { prop2: "租用休息室", prop3: "2小时/间", prop4: "400" },
  { prop2: "带棺火化B", prop3: "副", prop4: "380" },
  { prop2: "跨市县遗体接运", prop3: "公里", prop4: "3.5" },
  { prop2: "遗体火化", prop3: "具", prop4: "230" },
  { prop2: "出租拜祭房", prop3: "场", prop4: "480" },
  { prop2: "二次消毒", prop3: "具", prop4: "100" },
];
</script>

<style scoped>
.input-number {
  width: 120px;
}
</style>
