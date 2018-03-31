<template>
  <div>
    <el-row>
      <el-col :span="24" id="label-span">
        <span> <i class="el-icon-goods"></i>活跃见证人</span>
      </el-col>
    </el-row>
    <el-table
      :data="witnesses"
      stripe border
      style="width: 100%">
      <el-table-column
        prop="name"
        label="见证人">
      </el-table-column>
      <el-table-column
        prop="latestConfirmID"
        label="最近确认">
      </el-table-column>
      <el-table-column
        prop="totalVotes"
        label="总票数">
      </el-table-column>
    </el-table>
  </div>
</template>

<script>
export default {
  name: 'active-witnesses',
  data () {
    return {
      witnesses: [
        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        },

        {
          name: 'aaron',
          latestConfirmID: '123321',
          totalVotes: 2354323
        }
      ]
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
</style>
