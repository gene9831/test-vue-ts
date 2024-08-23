<template>
  <div style="padding: 10px">
    <el-button type="primary">员工安排</el-button>
    <el-button type="primary">出勤报表</el-button>
    <el-table :data="tableData" border style="width: 100%; margin-top: 15px">
      <el-table-column label="Date" width="300">
        <template #default="scope">
          <div style="display: flex; align-items: center; height: 80px">
            <el-icon><timer /></el-icon>
            <span style="margin-left: 10px">{{ scope.row.date }}</span>
          </div>
        </template>
      </el-table-column>
      <el-table-column label="9:00-11:00" min-width="300">
        <template #default="scope">
          <el-tag v-if="scope.row.nine">{{ scope.row.nine }}</el-tag>
        </template>
      </el-table-column>
      <el-table-column label="11:00-13:00" min-width="300">
        <template #default="scope">
          <el-tag v-if="scope.row.eleven">{{ scope.row.eleven }}</el-tag>
        </template>
      </el-table-column>
      <el-table-column label="13:00-15:00" min-width="300">
        <template #default="scope">
          <el-tag v-if="scope.row.thirteen">{{ scope.row.thirteen }}</el-tag>
        </template>
      </el-table-column>
      <el-table-column label="15:00-17:00" min-width="300">
        <template #default="scope">
          <el-tag v-if="scope.row.fifteen">{{ scope.row.fifteen }}</el-tag>
        </template>
      </el-table-column>
      <el-table-column label="17:00-19:00" min-width="300">
        <template #default="scope">
          <el-tag v-if="scope.row.seventeen">{{ scope.row.seventeen }}</el-tag>
        </template>
      </el-table-column>
    </el-table>
  </div>
</template>

<script lang="ts" setup>
import { Timer } from "@element-plus/icons-vue";

const tableData = [
  {
    date: "2024-05-03",
    nine: "张师傅",
    eleven: "",
    thirteen: "",
    fifteen: "",
    seventeen: "",
  },
  {
    date: "2024-05-04",
    nine: "",
    eleven: "",
    thirteen: "",
    fifteen: "李师傅",
    seventeen: "",
  },
  {
    date: "2024-05-05",
    nine: "",
    eleven: "",
    thirteen: "王师傅",
    fifteen: "",
    seventeen: "",
  },
  {
    date: "2024-05-06",
    nine: "",
    eleven: "",
    thirteen: "",
    fifteen: "赵师傅",
    seventeen: "",
  },
  {
    date: "2024-05-07",
    nine: "",
    eleven: "",
    thirteen: "",
    fifteen: "",
    seventeen: "孙师傅",
  },
  {
    date: "2024-05-08",
    nine: "",
    eleven: "胡师傅",
    thirteen: "",
    fifteen: "",
    seventeen: "",
  },
];
</script>
