<template>
  <div style="overflow: hidden">
    <el-row :gutter="20" justify="center">
      <el-col :span="6"
        ><div class="grid-content ep-bg-purple" />
        <el-form
          label-position="right"
          label-width="auto"
          :model="formLabelAlign"
          style="max-width: 600px"
        >
          <el-form-item label="出仓号">
            <el-input v-model="formLabelAlign.name" disabled />
          </el-form-item>
          <el-form-item label="物品类型">
            <el-input v-model="formLabelAlign.region" disabled />
          </el-form-item>
          <el-form-item label="物品编号">
            <el-input v-model="formLabelAlign.type" disabled />
          </el-form-item>
          <el-form-item label="单位">
            <el-input v-model="formLabelAlign.name" disabled />
          </el-form-item>
          <el-form-item label="数量">
            <el-input v-model="zeroVal" disabled />
          </el-form-item>
          <el-form-item label="经办部门">
            <el-input v-model="formLabelAlign.type" disabled />
          </el-form-item>
          <el-form-item label="载灰物标签">
            <el-input v-model="formLabelAlign.region" disabled />
          </el-form-item>
          <el-form-item label="性别">
            <el-input v-model="formLabelAlign.type" disabled />
          </el-form-item>
        </el-form>
      </el-col>
      <el-col :span="6"
        ><div class="grid-content ep-bg-purple" />
        <el-form
          label-position="right"
          label-width="auto"
          :model="formLabelAlign"
          style="max-width: 600px"
        >
          <el-form-item label="出仓日期" style="100%">
            <el-date-picker
              v-model="formLabelAlign.date"
              type="date"
              placeholder="出仓日期"
              style="width: 100%"
            />
          </el-form-item>
          <el-form-item label="物品名称">
            <el-input v-model="formLabelAlign.region" disabled />
          </el-form-item>
          <el-form-item label="供应商">
            <el-input v-model="formLabelAlign.type" disabled />
          </el-form-item>
          <el-form-item label="单价">
            <el-input v-model.number="zeroFVal" disabled />
          </el-form-item>
          <el-form-item label="总金额">
            <el-input v-model.number="zeroFVal" disabled />
          </el-form-item>
          <el-form-item label="经办人">
            <el-input v-model="formLabelAlign.type" disabled />
          </el-form-item>
          <el-form-item label="逝者姓名">
            <el-input v-model="formLabelAlign.region" disabled />
          </el-form-item>
          <el-form-item label="备注">
            <el-input v-model="formLabelAlign.type" disabled />
          </el-form-item>
        </el-form>
      </el-col>
    </el-row>
    <el-row :gutter="10" justify="center">
      <el-col :span="12">
        <el-card style="width: 100%">
          <el-result icon="info" title="请扫描商品条形码"> </el-result>
        </el-card>
      </el-col>
    </el-row>
    <el-row :gutter="20" justify="center">
      <el-col :span="12">
        <el-table :data="tableData" style="width: 100%; max-height: 1500px">
          <el-table-column prop="name" label="物品名称" width="180" />
          <el-table-column prop="unit" label="单位" width="180" />
          <el-table-column prop="quantity" label="数量" width="180">
            <template #default="scope">
              <el-input-number
                v-model="scope.row.quantity"
                :min="1"
                :max="10"
                @change="handleChange"
              />
            </template>
          </el-table-column>
          <el-table-column prop="number" label="编号" width="180" />
          <el-table-column label="操作">
            <template #default="scope">
              <el-button
                size="small"
                type="danger"
                @click="handleDelete(scope.$index, scope.row)"
              >
                Delete
              </el-button>
            </template>
          </el-table-column>
        </el-table>
      </el-col>
    </el-row>
    <div
      style="
        width: 100%;
        display: flex;
        justify-content: center;
        position: fixed;
        bottom: 100px;
      "
    >
      <el-button type="primary" style="width: 120px; height: 50px"
        >出仓</el-button
      >
    </div>
  </div>
</template>
<script lang="ts" setup>
import { reactive, ref } from "vue";
const zeroVal = "0";
const zeroFVal = "0.0";
const formLabelAlign = reactive({
  name: "",
  region: "",
  type: "",
});
const tableData = [
  {
    name: "纸钱",
    unit: "套",
    quantity: "2",
    number: "XXX",
  },
  {
    name: "寿衣",
    unit: "件",
    quantity: "3",
    number: "XXX",
  },
];
</script>

<style>
.el-row {
  margin-bottom: 20px;
}
.el-row:last-child {
  margin-bottom: 0;
}
.el-col {
  border-radius: 4px;
}

.grid-content {
  border-radius: 4px;
  min-height: 36px;
}
</style>
