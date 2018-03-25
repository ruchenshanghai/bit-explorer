<template>
  <header class="site-header">
    <el-row type="flex" justify="space-between">
      <el-col :span="6">
        <div class="grid-content">
          <img src="/static/favicon.ico"/>
          <p>{{corporationName}}</p>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content">
          <el-button type="primary" @click="aboutDialogVisible = true">关于我们</el-button>
        </div>
      </el-col>
    </el-row>
    <el-dialog
      title="九五尊易"
      :visible.sync="aboutDialogVisible"
      width="30%"
      :before-close="handleClose">
      <h3>九五尊易科技（香港）有限公司</h3>
      <h3>95isee Technology (Hongkong) Co., Ltd</h3>
      <h4>小鱼号：828256 企业QQ：599599528</h4>
      <h4>E-mail：95@95isee.com</h4>
      <h4>网站：www.95isee.com</h4>
      <span slot="footer" class="dialog-footer">
    <el-button type="primary" @click="aboutDialogVisible = false">确 定</el-button>
  </span>
    </el-dialog>
    <el-row type="flex" justify="center">
      <el-col :span="24">
        <h1>{{ mainTitleMsg }}</h1>
        <h2>{{ subTitleMsg }}</h2>
      </el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="12">
        <div class="el-container" id="search-input-container">
          <el-input placeholder="在此输入区块id、交易id、账户id或者账户名进行查询" v-model="searchText">
            <el-button slot="append" icon="el-icon-search"></el-button>
          </el-input>
        </div>
      </el-col>
    </el-row>
  </header>

</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      corporationName: '95isee',
      mainTitleMsg: 'Block Explorer',
      subTitleMsg: '提供区块、交易、账户等查询功能',
      aboutDialogVisible: false,
      searchText: ''
    }
  },
  methods: {
    handleClose (done) {
      this.$confirm('确认关闭？')
        .then(_ => {
          done()
        })
        .catch(_ => {
        })
    }
  }
}
</script>

<style scoped>
  .site-header {
    background-color: #1d8eca;
    color: #fff;
    padding: 10px;
  }

  .grid-content {
    vertical-align: center;
    color: white;
    border-radius: 4px;
    min-height: 36px;
  }

  h1 {
    font-weight: bolder;
    font-size: 3rem;
    line-height: 5rem;
  }

  #search-input-container {
    margin-top: 10px;
  }
</style>
