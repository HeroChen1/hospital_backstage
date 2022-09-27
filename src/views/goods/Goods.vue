<template>
  <div>
    <!-- 面包屑导航 -->
    <el-breadcrumb separator-class="el-icon-arrow-right">
      <el-breadcrumb-item :to="{ path: '/' }">首页</el-breadcrumb-item>
      <el-breadcrumb-item>科室设置</el-breadcrumb-item>
    </el-breadcrumb>
    <!-- 内容展示区域 -->
    <el-table :data="departmentData" border style="width: 100%" class="content">
      <el-table-column prop="name" label="名称" width="180"> </el-table-column>
      <el-table-column prop="establish" label="成立时间" width="180">
      </el-table-column>
      <el-table-column prop="countryCode" label="国家编码"> </el-table-column>
      <el-table-column prop="quota" label="额度"> </el-table-column>
      <el-table-column prop="bedCount" label="床数"> </el-table-column>
      <el-table-column prop="hospitalGrade" label="医院等级"> </el-table-column>
      <el-table-column prop="contacts" label="联系人"> </el-table-column>
      <el-table-column prop="phone" label="联系电话"> </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      // 科室信息数组
      departmentData: [
        {
          name: "名称",
          establish: "2000-06-06",
          countryCode: "99999",
          quota: "500万元",
          bedCount: "99",
          hospitalGrade: "一级",
          contacts: "联系人",
          phone: "110"
        }
      ]
    };
  }
};
</script>

<style scoped>
.content {
  margin-top: 20px;
}
</style>
