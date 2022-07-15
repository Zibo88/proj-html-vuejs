<template>
  <div>
    <MyHeader :links='menuLinks'/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'

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

      ]



    }
  },
  components: {
    MyHeader,
  }
}
</script>

<style lang="scss">
@import './style/common'

</style>
