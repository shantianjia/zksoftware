<template>
    <el-container style="height: 100%; border: 1px solid #eee">
  <el-aside width="100px" style="background-color: #409EFF;">
    <el-menu>
      <el-menu-item><a href="#"><i class="el-icon-s-custom left-icon-color"></i></a></el-menu-item>
      <el-menu-item><a href="#"><i class="el-icon-video-camera left-icon-color"></i></a></el-menu-item>
      <el-menu-item><a href="#"><i class="el-icon-notebook-2 left-icon-color"></i></a></el-menu-item>
      <el-menu-item><a href="#"><i class="el-icon-setting left-icon-color"></i></a></el-menu-item>
    </el-menu>
  </el-aside>
  
  <el-container>
    <el-header style="text-align: right; font-size: 12px">
      <el-dropdown>
        <i class="el-icon-setting" style="margin-right: 15px"></i>
        <el-dropdown-menu slot="dropdown">
          <el-dropdown-item>查看</el-dropdown-item>
          <el-dropdown-item>新增</el-dropdown-item>
          <el-dropdown-item>删除</el-dropdown-item>
        </el-dropdown-menu>
      </el-dropdown>
      <span>王小虎</span>
    </el-header>
    
    <el-main>
      <el-table :data="tableData">
        <el-table-column prop="date" label="日期" width="140">
        </el-table-column>
        <el-table-column prop="name" label="姓名" width="120">
        </el-table-column>
        <el-table-column prop="address" label="地址">
        </el-table-column>
      </el-table>
    </el-main>
  </el-container>
</el-container>

</template>

<style>
  .el-header {
    background-color: #B3C0D1;
    color: #333;
    line-height: 60px;
  }
  .el-menu-item{margin:30px 0;}
  .el-menu{background-color: #409EFF !important;}
  .el-aside {
    color: #333;
  }
  .left-icon-color{color: #fff !important; font-size: 40px !important;}
</style>

<script>
  export default {
    data() {
      const item = {
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄'
      };
      return {
        tableData: Array(20).fill(item)
      }
    }
  };
</script>