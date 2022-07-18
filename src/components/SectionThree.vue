<template>
    <div class="section-three-container">
            <h2>
                <span class="light-weight">Working</span>  <span class="italic">process</span>
            </h2>
            <!-- icone -->
            <div class="section-three-icon-container flex">

                <!-- item -->
                <div v-for="element in imgSectionThree" :key="element" class="icon flex">
                    <div class="square flex">
                        <img class="section-3-img" src="../assets/img/short-slider-rev-1-img-4.png" alt="section-3-img">
                    </div>
                    <h4>{{element.title}}</h4>
                    <div class="text">
                        {{element.text}}
                    </div>
                </div>
        
            </div>
            <img class="line" src="../assets/svg/svg-3.svg" alt="background-line">
        </div>
</template>

<script>
export default {
    name:'SectionThree',
    props:{
        imgSectionThree:Array
    }
   
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.section-three-container{
    position: relative;
    padding: $padding_section;
   

    & h2{
        margin: 20px 0 60px 0;
        font-size: 50px;
        padding-bottom: 50px;

    }
    
    & .line{
        width: 84%;
        margin: 0 auto;
        position: absolute;
        top: 237px;
        left: 55px;
    }
}
.section-three-icon-container.flex{
    z-index: 10;
    position: relative;
    padding-bottom: 50px;
    justify-content: center;

    & .icon.flex{
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: calc(100% / 4);
          margin:0 35px;

        & h4{
            padding: 10px 0;
            font-weight: 400;
            font-size: 18px;
        }

        & .text{
            font-size: 13px;
        }

        & .square.flex{
            background-color: #fbf7f1;
            justify-content: center;
            align-items: center;
            width: 150px;
            height: 150px;
            border-radius: 50%;

            & .section-3-img{
                width: 70px;
            }
        }
    }


    & .test{
        position: absolute;
    }
   
}

</style>