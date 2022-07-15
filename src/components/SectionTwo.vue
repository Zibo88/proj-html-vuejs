<template>
      <div>
         <!-- <ul class="list-second-section flex">
             <li class="item-second-section" v-for="poster in arrayImg" :key="poster">
                <img class="square" src="../assets/img/h-2-port-img-4.jpg" alt="">  -->
                <!-- //////////////// da sistemare ///////////////////// -->
                <!-- <img :src="`../assets/img/${this.poster.name}`" alt=""> -->
                <!-- ////////////////////////////////////////////////////// -->

                <!-- :hover -->
                <!-- <div class="features">
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
         </ul> -->
      </div>
</template>

<script>
export default {
    name:'SectionTwo',
    // props:{
    //     arrayImg: Array
    // },

}
</script>

<style lang="scss" scoped>
// @import '../style/common';
// @import '../style/variables';

// .section-two-container{
//     padding: $padding_section;

//     & .list-second-section.flex{
//         flex-wrap: wrap;
//     }
//     .item-second-section{
//         width: calc(100% / 3);
//         position: relative;

//         & .features{
//         width: 35%;
//         padding: 4px;
//         background-color: white;
//         position: absolute;
//         bottom:200px;
//         left: 0;
//         display: none;
//         & .features-title{
//             font-size: 18px;
//             padding: 5px 0;
//         }
//         & .features-illustration.text{
//             font-size: 14px;
//         }
//         }
//         // hover
//         &:hover .features{
//             display: block;
//         }

//     }
   

    
// }


</style>