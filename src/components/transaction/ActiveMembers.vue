<template>
  <div>
    <el-row>
      <el-col :span="24" id="label-span">
        <span> <i class="el-icon-view"></i>活跃理事会成员</span>
      </el-col>
    </el-row>
    <el-table
      :data="members"
      stripe border
      style="width: 100%">
      <el-table-column
        prop="name"
        label="账户">
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
  name: 'active-members',
  data () {
    return {
      members: [
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        },
        {
          name: 'thomas',
          totalVotes: 123465789
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
