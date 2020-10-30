<template>
    <div class="todolist">
        <h1>Todo List</h1>
        <input type="text" name="" id="" v-model="newTask">
        <button @click="todoList.push({name:newTask,disabled:false})">Thêm</button>
        <div class="list-item" v-for="(todo,index) in todoList" :key="index">
            <input type="checkbox" name="" id="list-todo" v-model="todo.disabled" class="checkboxx">
            <span class="item" for="list-todo" :class="{disable:todo.disabled}">{{todo.name}}</span>
        </div>
        
    </div>
</template>
<script>
export default {
    data:function(){
        return {
            newTask:'',
            todoList:[
                {name:'Đi chợ',disabled:false},
                {name:'Giặt đồ',disabled:false},
                {name:'Code',disabled:false},
                {name:'Đi ch***',disabled:false}
            ]
        }
    }
}
</script>
<style scoped>
.todolist{
    border: 1px solid red;
    width: 300px;
    margin: 0 auto;
}
.item{
    font-size: 20px;
    margin: 20px;
}
.checkboxx{
    display: inline-block;
    
}
.list-item{
    padding: 5px 0;
}
.disable{
    text-decoration: line-through;
}
</style>