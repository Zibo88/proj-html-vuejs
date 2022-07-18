<template>
  <div class="container">
    <MyHeader :links='menuLinks'/>
    <MainComponent/>
    <MyFooter/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MainComponent from './components/MainComponent.vue'
import MyFooter from './components/MyFooter.vue'

export default {
  name: 'App',
  data(){
    return{

      menuLinks:[

        {
          name:'Home',
          url:'#',
          currentElement: true,
        },
        {
          name:'Pages',
          url:'#',
          currentElement: false,
        },
         {
          name:'Portfolio',
          url:'#',
          currentElement: false,
        },
         {
          name:'Blog',
          url:'#',
          currentElement: false,
        },
         {
          name:'Shop',
          url:'#',
          currentElement: false,
        },
         {
          name:'Element',
          url:'#',
          currentElement: false,
        },

      ],

      

     

    }
  },
  components: {
    MyHeader,
    MainComponent,
    MyFooter
  }
}
</script>

<style lang="scss">
.container{
  max-width: 1440px;
}

</style>
