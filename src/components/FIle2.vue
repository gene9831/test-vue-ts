<template>
  <h2 style="text-align: center">已归档档案</h2>

  <div class="table-container">
    <div
      style="
        margin-bottom: 10px;
        display: flex;
        flex-direction: row;
        gap: 20px;
        justify-content: space-between;
      "
    >
      <div>
        <el-button type="primary">导出</el-button>
      </div>
      <div>
        <el-input placeholder="搜索内容" style="width: 240px"></el-input>
        <el-button :icon="Search" />
      </div>
    </div>
    <el-table style="width: 100%" :data="tableData">
      <el-table-column type="selection" width="55"> </el-table-column>

      <el-table-column prop="fileNumber" label="档案编号"></el-table-column>
      <el-table-column prop="time" label="归档时间"></el-table-column>
      <el-table-column prop="number" label="包含档案数量"></el-table-column>
      <el-table-column prop="admin" label="操作人"></el-table-column>

      <el-table-column label="操作">
        <el-button size="small">预览目录</el-button>
      </el-table-column>
    </el-table>
  </div>
</template>

<script setup lang="ts">
import { Search } from "@element-plus/icons-vue";
const tableData = [
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
  {
    fileNumber: 10000,
    number: 10,
    time: "2000-10-10",
    admin: "张三三",
  },
];
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 20px;
}
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 10px;
}
.search-container {
  display: flex;
  align-items: center;
}
.search-container .el-form-item {
  margin-right: 20px;
}
.el-form-item:last-child {
  margin-right: 0;
}
.el-table__header-wrapper {
  background-color: #dbe9f4 !important; /* 浅蓝色背景 */
}
.el-table th {
  text-align: center;
  font-weight: bold !important; /* 加粗字体 */
  background-color: #bee0f4 !important; /* 浅蓝色背景 */
  padding: 12px; /* 适当调整内边距 */
  white-space: nowrap;
  font-size: 15px; /* 调整字体大小 */
  color: #000; /* 黑色字体 */
}
.el-table td {
  text-align: center;
  padding: 10px;
  white-space: nowrap;
}
.el-table-column:nth-child(1),
.el-table-column:nth-child(2),
.el-table-column:nth-child(3),
.el-table-column:nth-child(4),
.el-table-column:nth-child(5),
.el-table-column:nth-child(6),
.el-table-column:nth-child(7),
.el-table-column:nth-child(8) {
  width: 80px;
}
.el-table-column:nth-child(9),
.el-table-column:nth-child(10),
.el-table-column:nth-child(11),
.el-table-column:nth-child(13),
.el-table-column:nth-child(14),
.el-table-column:nth-child(15) {
  width: 120px;
}
.el-table-column:nth-child(12),
.el-table-column:nth-child(16) {
  width: 180px;
}
.el-table-column:last-child {
  width: 250px;
}
.el-pagination {
  text-align: right;
  margin-top: 10px;
}
.el-button--reset {
  margin-left: 10px;
  background-color: #fff;
  color: #409eff;
  border-color: #dcdfe6;
}
</style>
