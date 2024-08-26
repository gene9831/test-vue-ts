<template>
  <h2 style="text-align: center">档案编辑</h2>

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
        <el-button type="primary">导入记录</el-button>
        <el-button type="primary">批量归档</el-button>
      </div>
      <div>
        <el-input placeholder="搜索内容" style="width: 240px"></el-input>
        <el-button :icon="Search" />
      </div>
    </div>
    <el-table style="width: 100%" :data="tableData">
      <el-table-column type="selection" width="55"> </el-table-column>

      <el-table-column prop="status" label="状态">
        <template #default="scope">
          <span
            :style="`color: ${scope.row.status === '可归档' ? 'green' : 'red'}`"
            >{{ scope.row.status }}</span
          >
        </template>
      </el-table-column>
      <el-table-column prop="fileNumber" label="资料编号"></el-table-column>
      <el-table-column prop="name" label="死者姓名"></el-table-column>
      <el-table-column prop="gender" label="性别"></el-table-column>
      <el-table-column prop="nation" label="名族"></el-table-column>
      <el-table-column prop="idnumber" label="死者证件号码"></el-table-column>
      <el-table-column prop="address" label="户籍地址"></el-table-column>
      <el-table-column prop="number1" label="火化证印刷号"></el-table-column>
      <el-table-column prop="deadtime" label="死亡时间"></el-table-column>
      <el-table-column prop="number2" label="死亡证编号"></el-table-column>
      <el-table-column prop="burntime" label="火化时间"></el-table-column>
      <el-table-column prop="contract" label="合同"></el-table-column>
      <el-table-column prop="person" label="领证人"></el-table-column>

      <el-table-column prop="attach" label="附件"></el-table-column>
      <el-table-column label="操作" width="150">
        <el-button type="primary" size="small">编辑</el-button>
        <el-button size="small">预览</el-button>
      </el-table-column>
    </el-table>
  </div>
</template>

<script setup lang="ts">
import { Search } from "@element-plus/icons-vue";
const tableData = [
  {
    status: "可归档",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
  },
  {
    status: "缺少资料",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
  },
  {
    status: "可归档",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
  },
  {
    status: "可归档",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
  },
  {
    status: "可归档",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
  },
  {
    status: "可归档",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
  },
  {
    status: "可归档",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
  },
  {
    status: "可归档",
    fileNumber: 10000,
    name: "张三",
    gender: "男",
    nation: "汉族",
    idnumber: "12345678901",
    address: "xxx",
    number1: "4412345",
    deadtime: "2000-10-10",
    number2: "D1234567",
    burntime: "2000-10-20",
    contract: "123456",
    person: "张三三",
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
