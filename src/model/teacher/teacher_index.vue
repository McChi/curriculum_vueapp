<template>
  <div class="teacherIndex">
    <div class="function">
      考核管理
      <div class="fun1">
        <el-row :gutter="12">
          <el-col :span="8">
            <el-card shadow="hover" @click.native="cardClick(1)">
              <i class="el-icon-s-order"></i>
              题库管理
            </el-card>
          </el-col>
          <el-col :span="8">
            <el-card shadow="hover" @click.native="cardClick(2)">
              <i class="el-icon-collection"></i>
              考试管理
            </el-card>
          </el-col>
        </el-row>
      </div>
      学习管理
      <div class="fun2">
        <el-row :gutter="12">
          <el-col :span="8">
            <el-card shadow="hover" @click.native="cardClick(3)">
              <i class="el-icon-user"></i>
              知识点管理
            </el-card>
          </el-col>
          <el-col :span="8">
            <el-card shadow="hover" @click.native="cardClick(4)">
              <i class="el-icon-user-solid"></i>
              查看学习情况
            </el-card>
          </el-col>
        </el-row>
      </div>
      系统管理
      <div class="fun2">
        <el-row :gutter="12">
          <el-col :span="8">
            <el-card shadow="hover" @click.native="cardClick(5)">
              <i class="el-icon-message-solid"></i>
              公告管理
            </el-card>
          </el-col>
        </el-row>
      </div>
      当前正在进行的考试
      <div class="exam">
      </div>
    </div>
  </div>
</template>

<script>
    export default {
      name: "teacher_index",
      data() {
        return {
          form: {
            name: '',
            region: '',
            date1: '',
            date2: '',
            delivery: false,
            type: [],
            resource: '',
            desc: ''
          }
        }
      },
      methods: {
        cardClick(flag) {
          switch (flag) {
            case 1: this.$router.push({ path: '/question_manage' });  break;
            case 2: this.$router.push({ path: '/exam_manage' });  break;
            case 3: this.$router.push({ path: '/' });  break;
            case 4: this.$router.push({ path: '/' });  break;
            case 5: this.$router.push({ path: '/notice_manage' });  break;
          }
        }
      }
    }
</script>

<style scoped>
  .teacherIndex{
    margin-top: 60px;
    float: right;
    background-color: #e3e3e3;
    min-height: 570px;
    width: 84%;
  }
  .function{
    padding: 40px 0 0 60px;
  }
  .fun1{
    margin-top: 5px;
    padding-top: 10px;
    border-top: solid #ACC0D8 1px;
  }
  .fun2{
    margin-top: 5px;
    padding-top: 10px;
    border-top: solid #ACC0D8 1px;
  }
  .exam{
    margin-top: 5px;
    padding-top: 10px;
    border-top: solid #ACC0D8 1px;
  }
  .el-col{
    margin-right: 40px;
    width: 220px;
    height: 100px;
    cursor:pointer;
  }
  .home_banner{position:relative;width:100%;height:620px;color:#fff;background:url("../../assets/image/banner.png") no-repeat center center;background-size:cover}

  .el-tabs__header{
    z-index: 0;
  }
  .el-table{
    z-index: 0;
  }
  .el-tab-pane{
    margin-left: 10px;
    margin-top: 10px;
  }
  .labelColor .el-form-item__label{
    color: #53514b;
  }
</style>
