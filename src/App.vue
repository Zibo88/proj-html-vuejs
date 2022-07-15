<template>
  <div>
    <MyHeader :links='menuLinks'/>
    <MainComponent :arrayImg='arrayImgSecondS'/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MainComponent from './components/MainComponent.vue'

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

      arrayImgSecondS:[
        {
          name:'h-2-port-img-1.jpg'
        },
        {
          name:'h-2-port-img-2.jpg'
        },
        {
          name:'h-2-port-img-3.jpg'
        },
        {
          name:'h-2-port-img-4.jpg'
        },
        {
          name:'h-2-port-img-5.jpg'
        },
        {
          name:'h-2-port-img-6.jpg'
        },
      ]

    }
  },
  components: {
    MyHeader,
    MainComponent
  }
}
</script>

<style lang="scss">


</style>
