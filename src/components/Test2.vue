<!-- 防腐冰柜看板 -->
<template>
  <h2 style="text-align: center">防腐冰柜看板</h2>

  <div style="margin: 20px">
    <div
      style="
        margin-bottom: 20px;
        font-size: small;
        color: #909399;
        display: flex;
        gap: 20px;
        align-items: center;
      "
    >
      <div>
        <span style="margin-right: 10px">时间</span>
        <el-date-picker type="datetime" placeholder="时间筛选" />
      </div>
      <div>
        <span style="margin-right: 10px">类型</span>
        <el-select placeholder="类型筛选" style="width: 240px"></el-select>
      </div>
      <div>
        <span style="margin-right: 10px">状态</span>
        <el-select placeholder="状态筛选" style="width: 240px"></el-select>
      </div>
    </div>
    <el-row :gutter="20" class="row row2">
      <el-col :span="2" v-for="i in 50">
        <div
          style="
            display: flex;
            flex-direction: column;
            gap: 10px;
            width: 100%;
            height: 100%;
          "
        >
          <div
            style="width: 100%; height: 100%; font-size: small"
            :class="[
              'cell-hgrtft',
              {
                finish: getType(i) === 'info',
                using: getType(i) === 'primary',
              },
            ]"
          >
            <div>防腐冰柜{{ i }}</div>
            <div v-if="getType(i) !== 'info'">编号：10000</div>
            <div v-if="getType(i) !== 'info'">死者姓名：张三</div>
            <div v-if="getType(i) === 'primary'">状态：正常使用中</div>
            <div v-if="getType(i) === 'primary'">温度：xxx</div>
            <div v-if="getType(i) === 'primary'">湿度：xxx</div>
            <div v-if="getType(i) === 'warning'">状态：温度偏高</div>
            <div v-if="getType(i) === 'warning'">温度：xxx</div>
            <div v-if="getType(i) === 'warning'">湿度：xxx</div>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script lang="ts" setup>
const using = [3, 4, 5];
const status2 = [10, 20];
const getType = (i: number) => {
  if (using.includes(i)) {
    return "primary";
  }

  if (status2.includes(i)) {
    return "warning";
  }

  return "info";
};
</script>

<style>
.row > div {
  border: 1px solid #e2e2e2;
  text-align: center;
}
.row2 > div {
  display: flex !important;
  align-items: center;
  justify-content: center;
  height: 150px;
  padding: 0 !important;
}
.a-button {
  width: 100% !important;
  height: 100% !important;
  margin: 0 !important;
}
</style>
