<template>
    <div class="header-menu">
        <img src="../assets/img/logo-sidearea-1.png" alt="logo">
        <ul>
            <li v-for="link in links" :key="link">
                {{link.name}}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name:'MyHeader',
    props:{
        links: Array
    }
}
</script>

<style lang="scss" scoped>

</style>