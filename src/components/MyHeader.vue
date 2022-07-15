<template>
    <div class="header-menu-container flex">
        <img class="header-logo" src="../assets/img/logo-sidearea-1.png" alt="">
        <ul class="header-menu flex">
            <li v-for="link,index in links" :key="index" class="menu-item" :class="{'current' : link.currentElement === true}">
                <a :href="link.url" >
                    {{link.name}} 
                </a>
            </li>
            <img class="hamburger-menu" src="../assets/svg/svg-1.svg" alt="icon-menu">
        </ul>
    </div>
</template>

<script>
export default {
    name:'MyHeader',
    props:{
        links:Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/common';

.header-menu-container.flex{
    padding: 30px;
    justify-content: space-between;
    align-items: center;
    height: 70px;
    .header-logo{
        width: 100px;
        cursor: pointer;
    }
    .menu-item{
        margin: 0 15px;
        font-size: 20px;
        
        & a{
            color: black;
        }
    }
}


</style>