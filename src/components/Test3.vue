<!-- 出柜预约 -->
<template>
  <h2 style="text-align: center">出柜预约</h2>

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
      <el-button type="primary" @click="dialogVisible = true"
        >新增预约</el-button
      >
      <el-dialog
        v-model="dialogVisible"
        title="新增预约"
        width="500"
        :before-close="handleClose"
      >
        <el-form label-width="auto" status-icon>
          <el-form-item label="资料编号" prop="name">
            <el-input />
          </el-form-item>
          <el-form-item label="死者姓名" prop="name">
            <el-input />
          </el-form-item>
          <el-form-item label="出柜预约时间" prop="name">
            <el-date-picker
              style="width: 100%"
              type="date"
              placeholder="选择日期"
            />
          </el-form-item>

          <el-form-item label="管理员" prop="name">
            <el-select placeholder="请选择管理员">
              <el-option label="管理员A" value="居民身份证" />
              <el-option label="管理员B" value="护照" />
            </el-select>
          </el-form-item>
          <el-form-item label="提尸员" prop="name">
            <el-select placeholder="请选择提尸员">
              <el-option label="提尸员A" value="居民身份证" />
              <el-option label="提尸员B" value="护照" />
            </el-select>
          </el-form-item>
        </el-form>
        <template #footer>
          <div class="dialog-footer">
            <el-button @click="dialogVisible = false">取消</el-button>
            <el-button type="primary" @click="dialogVisible = false">
              确认
            </el-button>
          </div>
        </template>
      </el-dialog>
      <div>
        <span style="margin-right: 10px">日期筛选</span>
        <el-date-picker type="date" placeholder="选择开始日期" />
        -
        <el-date-picker type="date" placeholder="选择结束日期" />
      </div>
      <div>
        <el-select placeholder="快速选择时间段" style="width: 150px">
          <el-option label="1天内" />
          <el-option label="3天内" />
          <el-option label="7天内" />
        </el-select>
      </div>
    </div>
    <el-row :gutter="20" class="row row1">
      <el-col :span="2"
        ><div class="grid-content ep-bg-purple" />
        时段</el-col
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
    <el-row :gutter="20" class="row row-3">
      <el-col :span="2">2024-08-01 周四(今天) </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2">
        <div class="cell-container">
          <el-button type="info" class="flex-btn">
            <span>编号：10000</span>
            <span>死者姓名：张三</span>
            <span>状态：已出柜</span>
          </el-button>
          <el-button type="info" class="flex-btn">
            <span>编号：10002</span>
            <span>死者姓名：张三</span>
            <span>状态：已出柜</span>
          </el-button>
          <el-button type="info" class="flex-btn">
            <span>编号：10003</span>
            <span>死者姓名：张三</span>
            <span>状态：已出柜</span>
          </el-button>
        </div>
      </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2">
        <div class="cell-container">
          <el-button type="primary" class="flex-btn">
            <span>编号：10000</span>
            <span>死者姓名：张三</span>
            <span>状态：已预约</span>
          </el-button>
        </div>
      </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
    </el-row>
    <el-row :gutter="20" class="row row-3">
      <el-col :span="2">2024-08-02 周五(明天) </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2">
        <div class="cell-container">
          <el-button type="primary" class="flex-btn">
            <span>编号：10000</span>
            <span>死者姓名：张三</span>
            <span>状态：已预约</span>
          </el-button>
          <el-button type="primary" class="flex-btn">
            <span>编号：10000</span>
            <span>死者姓名：张三</span>
            <span>状态：已预约</span>
          </el-button>
        </div></el-col
      >
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2">
        <div class="cell-container">
          <el-button type="primary" class="flex-btn">
            <span>编号：10000</span>
            <span>死者姓名：张三</span>
            <span>状态：已预约</span>
          </el-button>
        </div></el-col
      >
      <el-col :span="2"> </el-col> </el-row
    ><el-row :gutter="20" class="row row-3">
      <el-col :span="2">2024-08-03 周六</el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
      <el-col :span="2"> </el-col>
    </el-row>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { ElMessageBox } from "element-plus";

const dialogVisible = ref(false);

const handleClose = (done: () => void) => {
  ElMessageBox.confirm("Are you sure to close this dialog?")
    .then(() => {
      done();
    })
    .catch(() => {
      // catch error
    });
};
</script>

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
.row-3 > div {
  display: flex !important;
  align-items: center;
  justify-content: center;
  min-height: 150px !important;
}
.a-button {
  height: 50px !important;
  margin: 0 !important;
}
.cell-container {
  display: flex;
  flex-direction: column;
  gap: 8px;
  padding: 8px;
}
.flex-btn {
  margin: 0 !important;
  height: fit-content !important;
}
.flex-btn > span {
  display: flex;
  flex-direction: column;
  gap: 4px;
}
</style>
