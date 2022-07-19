<template>
   <main>

        <!-- prima sezione -->
        <section>
            <SectionOneComponent/>
        </section>
        <!-- seconda sezione -->
        <section>
            <!-- passo tramite props (arrayImg) l'array di immagini alla sezione 2 -->
            <SectionTwo :arrayImg='arrayImgSecondS' /> 
        </section>
        <!-- terza sezione -->
        <section>
             <!-- passo tramite props (imgSectionThree) l'array di immagini alla sezione 3 -->
            <SectionThree :imgSectionThree='arraySectionThree'/>
        </section>

        <section>
            <SectionFor/>
        </section>

        <section>
             <!-- passo tramite props (blogImg) l'array di immagini alla sezione 5 -->
            <SectionFive :blogImg='arraySectionFive'/>
        </section>

   </main>
</template>

<script>

import SectionOneComponent from './SectionOneComponent.vue'
import SectionTwo from './SectionTwo.vue'
import SectionThree from './SectionThree.vue'
import SectionFor from './SectionFor.vue'
import SectionFive from './SectionFive.vue'

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

            arraySectionThree:[
        {
            title:'First theres an idea',
            text:'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        },
        {
            title:'Then we talk about',
            text:'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        },
         {
            title:'And we think about',
            text:'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        },
        {
            title:'So we draw along',
            text:'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        },

        ],

        arraySectionFive:[
            {
                title: 'This way,loves: a detailed guide trough new design',
                author: 'By Emily Fields',
                img:'h-2-blog-img-1.jpg',
                day:'07',
                monthAndYear: "MAY '19'",
            },
            {
                title: 'I try to give people a different way of looking art',
                author: 'By Emily Fields',
                img:'h-2-blog-img-2.jpg',
                 day:'07',
                monthAndYear: "MAY '19'",
            },
            {
                title: 'Introduce Richard Laperrière of those amzig features',
                author: 'By Emily Fields',
                img:'h-2-blog-img-3.jpg',
                 day:'07',
                monthAndYear: "MAY '19'",
            },
        ]
      }

    },
    components:{
        SectionOneComponent,
        SectionTwo,
        SectionThree,
        SectionFor,
        SectionFive
    }
    
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';



</style>