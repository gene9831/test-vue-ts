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
        <span style="margin-right: 10px">预约时间</span>
        <el-date-picker type="datetime" placeholder="Select date and time" />
      </div>
    </div>
    <el-row :gutter="20" class="row row1">
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        洗礼室</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        08:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        09:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        10:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        11:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        12:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        13:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        14:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        15:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        16:30</el-col
      >
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        17:30</el-col
      >
    </el-row>
    <el-row :gutter="20" class="row row2">
      <el-col :span="2"> 洗礼室1 </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
    </el-row>

    <el-row :gutter="20" class="row row2">
      <el-col :span="2"> 洗礼室2 </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
    </el-row>
    <el-row :gutter="20" class="row row2">
      <el-col :span="2"> 洗礼室3 </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px">
          <el-button type="primary" size="large" class="a-button"
            >已预约</el-button
          >
        </div>
      </el-col>
      <el-col :span="2">
        <div style="display: flex; flex-direction: column; gap: 10px"></div>
      </el-col>
    </el-row>
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
</style>
