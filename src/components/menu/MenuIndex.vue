<template>
<div>
    <el-container>
      <el-header style="padding: 0px;display:flex;justify-content:space-between;align-items: center">
        <div style="display: inline">
          <el-input
            placeholder="通过菜单名称搜索,记得回车...."
            clearable
            @change="keywordsChange"
            style="width: 300px;margin: 0px;padding: 0px;"
            size="mini"
            @keyup.enter.native="searchMenuList"
            prefix-icon="el-icon-search"
            v-model="name">
          </el-input>
          <el-button type="primary" size="mini" style="margin-left: 5px" icon="el-icon-search" @click="searchMenuList">搜索
          </el-button>
        </div>
      </el-header>


    </el-container>

</div>


</template>

<script>
    export default {
        name: "MenuIndex",
      data() {
        return {
          name:'',
          menu :{
            id:'',
            url:'',
            path:'',
            name:'',
            iconCls:'',
            parentId:'',
            enabled:''
          }

        }

      },
      methods: {
        keywordsChange(val){
          if (val == '') {
            this.searchMenuList();
          }
        },
        searchMenuList(){

        },

      }
    }
</script>

<style scoped>

</style>
