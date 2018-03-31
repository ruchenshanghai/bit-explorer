<template>
  <div>
    <el-row>
      <el-col :span="24" id="label-span">
        <span>最新状态： </span>
        上次更新时间: {{ latestInterval }} 秒前
      </el-col>
    </el-row>
    <el-row type="flex" class="content-row">
      <el-col :span="24">
        <i class="el-icon-loading"></i>区块信息
      </el-col>
    </el-row>
    <el-row type="flex" class="content-row">
      <el-col :span="6">
        <i class="el-icon-tickets"></i>最新区块
      </el-col>
      <el-col :span="6">
        <a href="#">{{latestBlock.id}}</a>
      </el-col>
      <el-col :span="6">
        <i class="el-icon-document"></i>最新不可逆区块
      </el-col>
      <el-col :span="6">
        <a href="#">{{latestIrreversibleBlock.id}}</a>
      </el-col>
    </el-row>
    <el-row type="flex" class="content-row">
      <el-col :span="6">
        <i class="el-icon-refresh"></i>出块时间(秒)
      </el-col>
      <el-col :span="6">
        {{production.time}}
      </el-col>
      <el-col :span="6">
        <i class="el-icon-delete"></i>最近缺失
      </el-col>
      <el-col :span="6">
        {{production.missing}}
      </el-col>
    </el-row>
    <el-row type="flex" class="content-row">
      <el-col :span="6">
        <i class="el-icon-info"></i>总发行
      </el-col>
      <el-col :span="6">
        {{production.totalAmount.toLocaleString()}} GXS
      </el-col>
      <el-col :span="6">
        <i class="el-icon-success"></i>当前供给
      </el-col>
      <el-col :span="6">
        {{production.supplyAmount.toLocaleString()}} GXS
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  name: 'latest-block',
  data () {
    return {
      latestInterval: 0,
      latestBlock: {
        id: 123321
      },
      latestIrreversibleBlock: {
        id: 456654
      },
      production: {
        time: 4,
        missing: 5,
        totalAmount: 123456789,
        supplyAmount: 100000
      }
    }
  },
  created () {
    this.startUpdateInterval()
  },
  methods: {
    startUpdateInterval () {
      const self = this
      setInterval(function () {
        self.latestInterval++
        self.latestInterval %= 5
      }, 1000)
    }
  }
}
</script>

<style scoped>
  #label-span span {
    font-size: 1.5rem;
  }
  #label-span {
    padding-bottom: 5px;
    border-bottom: 1px solid #F5F5F5;
  }
  .content-row {
    background-color: #f9fafc;
    color: #333;
  }
  .content-row div {
    padding: 10px 5px;
    border: 1px solid #ddd;
  }
  .content-row a {
    text-decoration: none;
  }
</style>
