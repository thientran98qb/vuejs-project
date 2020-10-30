<template>
  <div id="app">
    <Navbar :menuData="menus" />
    <Task />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Task from './components/Task.vue'
export default {
  name: 'App',
  data:function(){
    return {
      menus:[
        { title:'Trang Chủ',status:false},
        { title:'Bài viết hay',status:false},
        { title:'Chuyện bên lề',status:false},
        { title:'Chuyện cuộc sống',status:false}
      ]
    }
  },
  components: {
    Navbar,
    Task
  }
}
</script>

<style>
body{
  padding: 0;
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;
  padding-top: 0;
}
</style>
