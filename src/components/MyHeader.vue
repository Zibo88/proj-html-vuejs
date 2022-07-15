<template>
    <!-- container header -->
    <div class="header-menu-container flex">
        <!-- logo -->
        <img class="header-logo" src="../assets/img/logo-sidearea-1.png" alt="">
        <!-- lista di link dell'header menu -->
        <ul class="header-menu flex">
            <!-- eseguo un ciclo for di ogni li per stampare tante li quanti sono gli oggetti trasferiti tramite props LINKS da App.vue -->
            <!-- Assegno la classe current solo se link.currentElement è vera -->
            <li v-for="link,index in links" :key="index" class="menu-item" :class="{'current' : link.currentElement === true}">
                <a :href="link.url" >
                    {{link.name}} 
                </a>
            </li>
            <!-- hamburger menu -->
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
    width: 95%;
    margin: 0 auto;
    justify-content: space-between;
    align-items: center;
    .header-logo{
        width: 100px;
        cursor: pointer;
    }
    .menu-item{
        margin: 0 15px;
        font-size: 20px;

        &:hover a {
            color: $utility_color;
        }
        
        & a{
            color: black;
        }
    }
}


</style>