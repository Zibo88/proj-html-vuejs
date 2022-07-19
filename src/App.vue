<template>
  <div class="container">
    <!-- passo tramite props  l'array contenente i link dei menù  -->
    <MyHeader :links='menuLinks'/>
    <MainComponent/>
    <!-- passo tramite props (info) l'Object footerObject contenente le info da stampare nel footer, tramite una props (socialIcon) passo l'array socialArray contenente le icone social (platform ha come valore la classe di fontawsome)  -->
    <MyFooter :info='footerObject' :socialIcon="socialArray"/>
  </div>
</template>

<script>
// importo le varie componenti
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
        img:'logo-sidearea-1.png',
        slogan: "Let's Get Creative",
        email:'maree.qode@gmail.com',
        telephone: '+44645 321 789',
        address: "Avenue d'Auderghem",
        city: '1040 Brussels, Belgium',
        socialTitle:'Stay in touch with us'
      },

      socialArray:[
        {
          platform: 'fa-brands fa-twitter',
        },
        {
          platform: 'fa-brands fa-pinterest-p',
        },
        {
          platform: 'fa-brands fa-facebook-f',
        },
        {
          platform: 'fa-brands fa-linkedin-in',
        }
      ] 
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
