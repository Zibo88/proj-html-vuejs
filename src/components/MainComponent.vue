<template>
   <div>
       <!-- prima sezione -->
       <div>
           <section>
                <SectionOneComponent/>
           </section>
       </div>
       <!-- seconda sezione -->
        <div class="section-two-container">
            <ul class="list-second-section flex">
                <li class="item-second-section" v-for="poster in arrayImg" :key="poster">
                    <img class="square" src="../assets/img/h-2-port-img-4.jpg" alt="">
                    <!-- //////////////// da sistemare ///////////////////// -->
                    <!-- <img :src="`../assets/img/${this.poster.name}`" alt=""> -->
                    <!-- ////////////////////////////////////////////////////// -->

                    <!-- :hover -->
                     <div class="features">
                        <h4 class="features-title">
                            Illustrations of novel   
                        </h4>

                        <div class="features-illustration text">
                            <em>
                                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                            </em>
                        </div>

                    </div>
                </li>
            </ul>
        </div> 
        <!-- <SectionTwo/> -->
   </div>
</template>

<script>

import SectionOneComponent from './SectionOneComponent.vue'
// import SectionTwo from './SectionTwo.vue'

export default {
    name:'MainComponent',
    data(){
        return{

        }
    },
    // methods:{
    //     createCard(){
    //         let finalImg = '../assets/img/' + this.poster.name 
    //         console.log(this.poster.name)
    //         return finalImg
    //     }
    // },
    props:{
        arrayImg: Array
    },
    components:{
        SectionOneComponent,
        // SectionTwo
    }
    

  
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.section-two-container{
    padding: $padding_section;

    & .list-second-section.flex{
        flex-wrap: wrap;
    }
    .item-second-section{
        width: calc(100% / 3);
        position: relative;

        & .features{
        width: 35%;
        padding: 4px;
        background-color: white;
        position: absolute;
        bottom:200px;
        left: 0;
        display: none;
        & .features-title{
            font-size: 18px;
            padding: 5px 0;
        }
        & .features-illustration.text{
            font-size: 14px;
        }
        }
        // hover
        &:hover .features{
            display: block;
        }
    }
  
}


</style>