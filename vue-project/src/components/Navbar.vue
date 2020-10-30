<template>
    <div class="navbar">
        <div class="navbar__logo">
            <a href="">
                <img alt="Vue logo" class="navbar__logo-img" src="../assets/logo.png">
            <h1 class="navbar__logo-title">S<span class="navbar__logo-title-special">O</span>F<span class="navbar__logo-title-special">T</span></h1>
            </a>
        </div>
        <ul class="navbar__list">
            <li class="navbar__list-item"  v-for="(menu,index) in menuData" :key="index"><a href="">{{menu.title}}</a></li>
        </ul>
    </div>
</template>
<script>
export default {
    props:{
        menuData:Object
    }
    ,
    data:function(){
        return {
            
        }
    }
}
</script>
<style scoped>
    .navbar{
        display: flex;
        justify-content: space-between;
        background: rgba(245, 170, 66);
    }
    .navbar__logo-img{
        width: 50px;
        margin-left: 20px;
        transform: translateY(10%);
    }
    .navbar__logo-title{
        display: inline-block;
        margin: 0;
        transform: translateY(-25%);
    }
    .navbar__logo-title-special{
        color: red;
        font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    }
    ul.navbar__list{
        list-style: none;
        display: flex;
    }
    ul.navbar__list .navbar__list-item{
        display: inline-block;
    }
    ul.navbar__list .navbar__list-item > a{
        text-decoration: none;
        padding: 25px 20px;
        color: white;
        font-weight: 600;

    }
    ul.navbar__list .navbar__list-item > a:hover{
       color: #d4d4d4;
    }
</style>