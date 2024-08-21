<template>
  <h2 style="text-align: center">大表单</h2>

  <div
    style="
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
    "
  >
    <el-steps
      style="width: 600px; padding-left: 100px"
      :space="200"
      :active="0"
      finish-status="success"
    >
      <el-step title="基础信息" />
      <el-step title="其他信息" />
      <el-step title="收费项目" />
    </el-steps>
    <el-form
      ref="ruleFormRef"
      style="width: 800px"
      :model="ruleForm"
      label-width="auto"
      class="demo-ruleForm"
      :size="formSize"
      status-icon
    >
      <el-form-item label="死者姓名" prop="name">
        <el-input v-model="ruleForm.name" />
      </el-form-item>
      <div style="display: flex">
        <el-col :span="10">
          <el-form-item label="证件类型" prop="region">
            <el-select v-model="ruleForm.region" placeholder="证件类型">
              <el-option label="居民身份证" value="居民身份证" />
              <el-option label="护照" value="护照" />
            </el-select>
          </el-form-item>
        </el-col>
        <el-col :span="14">
          <el-form-item label="证件号码">
            <el-input />
          </el-form-item>
        </el-col>
      </div>
      <div style="display: flex">
        <el-col :span="12">
          <el-form-item label="籍贯" prop="name">
            <el-input v-model="ruleForm.name" />
          </el-form-item>
        </el-col>
        <el-col :span="12">
          <el-form-item label="民族" prop="name">
            <el-input v-model="ruleForm.name" />
          </el-form-item>
        </el-col>
      </div>

      <el-form-item label="到达时间" required>
        <el-form-item prop="date1">
          <el-date-picker
            v-model="ruleForm.date1"
            type="date"
            placeholder="选择时间"
            style="width: 100%"
          />
        </el-form-item>
      </el-form-item>
      <el-form-item label="属地" required>
        <el-select v-model="ruleForm.region" placeholder="属地">
          <el-option label="居民身份证" value="居民身份证" />
          <el-option label="护照" value="护照" />
        </el-select>
      </el-form-item>
      <el-form-item label="死亡地点" required>
        <el-select v-model="ruleForm.region" placeholder="死亡地点">
          <el-option label="居民身份证" value="居民身份证" />
          <el-option label="护照" value="护照" />
        </el-select>
      </el-form-item>
      <div class="next">
        <el-button type="primary">下一步</el-button>
        <el-button type="primary">保存</el-button>
      </div>
    </el-form>
  </div>

  <div
    style="
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 20px;
    "
  >
    <el-steps
      style="width: 600px; padding-left: 100px"
      :space="200"
      :active="1"
      finish-status="success"
    >
      <el-step title="基础信息" />
      <el-step title="其他信息" />
      <el-step title="收费项目" />
    </el-steps>
    <el-form
      ref="ruleFormRef"
      style="width: 800px"
      :model="ruleForm"
      label-width="auto"
      class="demo-ruleForm"
      :size="formSize"
      status-icon
    >
      <el-form-item label="汽车停点" prop="name">
        <el-input v-model="ruleForm.name" />
      </el-form-item>
      <el-form-item label="死亡证号" prop="name">
        <el-input v-model="ruleForm.name" />
      </el-form-item>

      <el-form-item label="职业">
        <el-select v-model="ruleForm.region" placeholder="职业">
          <el-option label="居民身份证" value="居民身份证" />
          <el-option label="护照" value="护照" />
        </el-select>
      </el-form-item>
      <el-form-item label="收敛地点" prop="name">
        <el-input v-model="ruleForm.name" />
      </el-form-item>
      <div style="display: flex">
        <el-col :span="10">
          <el-form-item label="告别仪式">
            <el-form-item prop="date1">
              <el-date-picker
                v-model="ruleForm.date1"
                type="date"
                placeholder="选择时间"
                style="width: 100%"
              />
            </el-form-item>
          </el-form-item>
        </el-col>
        <el-col :span="14">
          <el-form-item label="告别厅">
            <el-select v-model="ruleForm.region" placeholder="告别厅">
              <el-option label="居民身份证" value="居民身份证" />
              <el-option label="护照" value="护照" />
            </el-select> </el-form-item
        ></el-col>
      </div>
      <el-form-item label="火化时间">
        <el-form-item prop="date1">
          <el-date-picker
            v-model="ruleForm.date1"
            type="date"
            placeholder="选择时间"
            style="width: 100%"
          />
        </el-form-item>
      </el-form-item>
      <el-form-item label="备注" prop="name">
        <el-input type="textarea" v-model="ruleForm.name" />
      </el-form-item>
      <div class="next">
        <el-button type="primary">下一步</el-button>
        <el-button type="primary">保存</el-button>
        <el-button>上一步</el-button>
      </div>
    </el-form>
  </div>
</template>

<script lang="ts" setup>
import type { ComponentSize, FormInstance } from "element-plus";
import { reactive, ref } from "vue";

interface RuleForm {
  name: string;
  region: string;
  count: string;
  date1: string;
  date2: string;
  delivery: boolean;
  location: string;
  type: string[];
  resource: string;
  desc: string;
}

const formSize = ref<ComponentSize>("default");
const ruleFormRef = ref<FormInstance>();
const ruleForm = reactive<RuleForm>({
  name: "",
  region: "",
  count: "",
  date1: "",
  date2: "",
  delivery: false,
  location: "",
  type: [],
  resource: "",
  desc: "",
});
</script>

<style scoped>
.next {
  display: flex;
  flex-direction: row-reverse;
  gap: 20px;
}
</style>
