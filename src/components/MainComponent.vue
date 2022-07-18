<template>
   <main>
        <!-- prima sezione -->
        <section>
            <SectionOneComponent/>
        </section>
        <!-- seconda sezione -->
        <section>
            <SectionTwo :arrayImg='arrayImgSecondS' /> 
        </section>
        <!-- terza sezione -->
        <section>
            <SectionThree :imgSectionThree='arraySectionThree'/>
        </section>

        <section>
            <SectionFor/>
        </section>

        <section>
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
            imgLink: 'data:image/png;base64,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',
            text:'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        },
        {
            title:'Then we talk about',
            imgLink: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTnDTfwFvFe11WA-XqEG_SVWnyZtW6ioWd76A&usqp=CAU',
            text:'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        },
         {
            title:'And we think about',
            imgLink: 'data:image/png;base64,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',
            text:'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
        },
        {
            title:'So we draw along',
            imgLink: 'data:image/png;base64,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',
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