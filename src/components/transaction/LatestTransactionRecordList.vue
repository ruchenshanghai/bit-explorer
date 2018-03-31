<template>
  <div>
    <el-row>
      <el-col :span="24" id="label-span">
        <span> <i class="el-icon-goods"></i>最新交易记录</span>
      </el-col>
    </el-row>
    <el-table
      :data="transactionRecords"
      stripe border
      style="width: 100%">
      <el-table-column
        prop="type"
        label="类型"
        width="180">
      </el-table-column>
      <el-table-column
        prop="content"
        label="内容">
      </el-table-column>
      <el-table-column
        prop="time"
        label="时间"
        width="180">
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: 'latest-transaction-record-list',
  data () {
    return {
      transactionRecords: [
        {
          type: '数据支付',
          content: 'opengateway 验证了数据源 cxsj 的数据上传',
          time: '刚刚'
        },
        {
          type: '数据支付',
          content: 'opengateway 验证了数据源 cxsj 的数据上传',
          time: '刚刚'
        },
        {
          type: '数据支付',
          content: 'opengateway 验证了数据源 cxsj 的数据上传',
          time: '刚刚'
        },
        {
          type: '数据支付',
          content: 'opengateway 验证了数据源 cxsj 的数据上传',
          time: '刚刚'
        },
        {
          type: '数据支付',
          content: 'opengateway 验证了数据源 cxsj 的数据上传',
          time: '刚刚'
        },
        {
          type: '发起数据交易',
          content: 'uy-jhxd 发起了一笔数据交易请求 ',
          time: '5秒前'
        },
        {
          type: '发起数据交易',
          content: 'uy-jhxd 发起了一笔数据交易请求',
          time: '5秒前'
        },
        {
          type: '发起数据交易',
          content: 'uy-jhxd 发起了一笔数据交易请求 ',
          time: '5秒前'
        },
        {
          type: '发起数据交易',
          content: 'uy-jhxd 发起了一笔数据交易请求 ',
          time: '5秒前'
        },
        {
          type: '发起数据交易',
          content: 'uy-jhxd 发起了一笔数据交易请求 ',
          time: '5秒前'
        },
        {
          type: '数据存证',
          content: 'opengateway 验证了数据源 cxsj 的数据上传 ',
          time: '5秒前'
        },
        {
          type: '数据存证',
          content: 'opengateway 验证了数据源 cxsj 的数据上传 ',
          time: '5秒前'
        },
        {
          type: '数据存证',
          content: 'opengateway 验证了数据源 cxsj 的数据上传 ',
          time: '5秒前'
        },
        {
          type: '数据存证',
          content: 'opengateway 验证了数据源 cxsj 的数据上传 ',
          time: '5秒前'
        },
        {
          type: '数据存证',
          content: 'opengateway 验证了数据源 cxsj 的数据上传 ',
          time: '5秒前'
        },
        {
          type: '转账',
          content: '发送 0.50000 GXS 到',
          time: '刚刚'
        },
        {
          type: '转账',
          content: '发送 0.50000 GXS 到',
          time: '刚刚'
        },
        {
          type: '转账',
          content: '发送 0.50000 GXS 到',
          time: '刚刚'
        },
        {
          type: '转账',
          content: '发送 0.50000 GXS 到',
          time: '刚刚'
        },
        {
          type: '转账',
          content: '发送 0.50000 GXS 到',
          time: '刚刚'
        }
      ]
    }
  },
  created () {
  },
  methods: {
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
</style>
