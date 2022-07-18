<template>
  <div class="container">
    <MyHeader :links='menuLinks'/>
    <MainComponent/>
    <MyFooter :info='footerObject'/>
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

      footerObject:{
        img:'../assets/imglogo-sidearea-1.png',
        slogan: "Let's Get Creative",
        email:'maree.qode@gmail.com',
        telephone: '+44645 321 789',
        address: "Avenue d'Auderghem",
        city: '1040 Brussels, Belgium',
        socialTitle:'Stay in touch with us'
        
      }
       
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
