<template>
  <h2 style="text-align: center">预约厅安排</h2>

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
      <el-button type="primary">新增预约</el-button>
      <div>
        <span style="margin-right: 10px">日期筛选</span>
        <el-date-picker type="date" placeholder="选择日期" />
      </div>
    </div>
    <div class="gridx">
      <div class="header">时段</div>
      <div class="header">崇惠厅(小)</div>
      <div class="header">崇晴厅(中)</div>
      <div class="header">崇慈厅(中)</div>
      <div class="header">崇康厅(大)</div>
      <div class="header">崇瑞厅(大)</div>
      <div class="header">崇贤厅(大)</div>
      <div class="header">崇德厅(大)</div>
      <div class="aaa">08:00</div>
      <div class="bbb"></div>
      <div
        class="bbb"
        style="grid-row: 3 / 5; grid-column: 2; background-color: #409eff"
      >
        <div>编号：200000</div>
        <div>死者姓名：张三</div>

        <div>状态: 使用中</div>
      </div>
      <div
        class="bbb"
        style="grid-row: 2 / 4; grid-column: 5; background-color: #909399"
      >
        <div>编号：200000</div>
        <div>死者姓名：张三</div>

        <div>状态: 已完成</div>
      </div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="aaa">08:30</div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="aaa">09:00</div>
      <div class="bbb"></div>
      <div
        class="bbb"
        style="grid-row: 5 / 7; grid-column: 3; background-color: #e6a23c"
      >
        <div>编号：200001</div>
        <div>死者姓名：张三</div>

        <div>状态: 已预约</div>
      </div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>

      <div class="bbb"></div>
      <div class="aaa">09:30</div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="aaa">10:00</div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="aaa">10:30</div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="aaa">11:00</div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="aaa">11:30</div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
      <div class="bbb"></div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>

<style>
.row1 {
  color: #909399;
}
.row1 > div {
  padding-top: 10px;
  padding-bottom: 10px;
  font-weight: bold;
}
.row > div {
  border: 1px solid #e2e2e2;
  text-align: center;
}
.row2 > div {
  display: flex !important;
  align-items: center;
  justify-content: center;
  height: 150px;
}
.a-button {
  height: 50px !important;
  margin: 0 !important;
}
.gridx {
  display: grid;
  grid-template-columns: repeat(8, 1fr);
}
.gridx > .header {
  font-weight: bold;
  color: #909399;
  padding: 10px;
  border: 1px solid #e2e2e2;
  text-align: center;
}
.gridx > div {
  padding: 10px;
  border: 1px solid #e2e2e2;
  text-align: center;
}
.gridx > .bbb {
  color: white;
}
</style>
