<template>
  <div id="app">
    <div>
      <Header></Header>
      <div class="container">
        <Add :add_App="add_App"></Add>
        <List :commends="commends" :delete_App="delete_App"></List>
      </div>
    </div>
  </div>
</template>

<script>
import { default as Header } from "./components/Header";
import { default as Add } from "./components/Add";
import List from "./components/List";
export default {
  name: "App",
  components: {
    Header,
    Add,
    List,
  },
  data(){
    return {
      commends:[
        {id:1,name:"提莫哥",content:"塔姆哥哥你真坏"},
        {id:2,name:"塔姆老弟",content:"提莫妹妹你身材真好"},
        {id:3,name:"盲僧",content:"你倒是接大啊"}
      ]
      }
    },
    methods:{
      add_App(o){
        this.commends.unshift(o);
      },
      delete_App(index){
        this.commends.splice(index,1);
      }
    }
};
</script>

<style scoped>
</style>
