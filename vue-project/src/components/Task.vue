<template>
    <div class="task__area">
       <div class="list">
           <div v-for="(langague,index) in langagues" :key="index" class="list__item" >
               <span class="list__item-value" :class="{selected: langague.selected}" @click="langague.selected =! langague.selected">{{ langague.name }}</span>
           </div>
       </div>
    </div>
</template>
<script>
export default {
    data:function(){
        return {
            langagues:[
                {name:'php', selected:false},
                {name:'js', selected:false},
                {name:'html', selected:false},
                {name:'css', selected:false},
                {name:'nodejs', selected:false}
            ]
        }
    }
}
</script>
<style scoped>
    .list__item{
        display: inline-block;
        padding: 20px 0;
    }
    .list__item-value{
        padding: 5px 20px;
        border: 2px solid red;
        border-radius: 5px;
        margin-right: 10px;
        outline: none;
    }
    .selected{
        background-color: green;
        color: white;
        border: none;
    }
</style>