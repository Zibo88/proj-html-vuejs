<template>
   <div>
        <!-- prima sezione -->
        <section>
            <SectionOneComponent/>
        </section>
        <!-- seconda sezione -->
        <section>
            <SectionTwo :arrayImg='arrayImgSecondS'/> 
        </section>
        <!-- terza sezione -->
        <section>
            <SectionThree/>
        </section>
   </div>
      
  

</template>

<script>

import SectionOneComponent from './SectionOneComponent.vue'
import SectionTwo from './SectionTwo.vue'

import SectionThree from './SectionThree.vue'

export default {
    name:'MainComponent',
    data(){
        return{
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
      ],

        }
    },
    components:{
        SectionOneComponent,
        SectionTwo,
        SectionThree
    }
    
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

// Sezione due


// SEZIONE TRE
.section-three-container{
    width: 60%;
    margin: 0 auto;
    text-align: center;
    padding: $padding_section;

    & h2 {
        font-size: 30px;
        padding-bottom: 20px;
    }

    .svg-test{
        background-color: pink;
        color: green;
    }

}


</style>