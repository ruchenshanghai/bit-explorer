<template>
  <el-container>
    <el-aside width="300px">
      <div id="aside-container">
        <active-witnesses></active-witnesses>
        <active-members></active-members>
      </div>
    </el-aside>
    <el-main>
      <latest-transaction-record-list></latest-transaction-record-list>
    </el-main>
  </el-container>
</template>

<script>
import latestTransactionRecordList from './transaction/LatestTransactionRecordList'
import activeWitnesses from './transaction/ActiveWitnesses'
import activeMembers from './transaction/ActiveMembers'

export default {
  name: 'latest-transactions',
  components: {
    LatestTransactionRecordList: latestTransactionRecordList,
    ActiveWitnesses: activeWitnesses,
    ActiveMembers: activeMembers
  }
}
</script>

<style scoped>
#aside-container {
  padding: 20px;
}
#aside-container div {
  margin-bottom: 50px;
}
</style>
