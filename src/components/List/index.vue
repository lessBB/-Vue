<template>
  <div class="col-md-8">
    <h3 class="reply">评论回复：</h3>
    <h2 style="display: none">暂无评论，点击左侧添加评论！！！</h2>
    <ul class="list-group">
        <!-- 列表渲染 -->
      <Item v-for="(commend,index) in commends" :key="commend.id" :commend="commend" :index="index" :delete_App="delete_App"></Item>
    </ul>
  </div>
</template>

<script>
import Item from "./Item";
export default {
  name: "List",
  props:["commends","delete_App"],
  components: {
    Item
  },
};
</script>

<style scoped>
.reply {
  margin-top: 0px;
}
</style>
