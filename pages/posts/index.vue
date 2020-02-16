<template>
  <section class="container posts-page">
    <el-card>
      <div slot="header" class="clearfix">
        <span>新着投稿</span>
      </div>
      <el-table
        :data="showPosts"
        style="width: 100%"
        class="table"
      >
        <el-table-column
          prop="title"
          label="タイトル"
        >
        </el-table-column>
        <el-table-column
          prop="user.id"
          label="投稿者"
          width="180"
        >
        </el-table-column>
        <el-table-column
          prop="created_at"
          label="投稿日時"
          width="240"
        >
        </el-table-column>
      </el-table>
    </el-card>
  </section>
</template>


<script>
export default {
  computed: {
    showPosts() {
      return [
        {
          id: '001',
          title: 'How to ...',
          body: 'body',
          created_at: '2020/02/03 12:23:55',
          user: {
            id: 'hoge'
          }
        },
        {
          id: '002',
          title: 'How to 2...',
          body: 'body 2',
          created_at: '2020/02/04 12:23:55',
          user: {
            id: 'hoge'
          }
        },
      ]
    }
  }
}
</script>

<style>
.posts-page  .el-table_row {
  cursor: pointer;
}
</style>
