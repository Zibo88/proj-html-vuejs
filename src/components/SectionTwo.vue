<template>
       <div class="section-two-container">
            <ul class="list-second-section flex">

                <!-- eseguo un ciclo for per ogni immagine presente in arrayImg -->
                <li class="item-second-section" v-for="(element, index) in arrayImg" :key="index">
                    <!-- img -->
                     <img :src="require(`../assets/img/${element.name}`)" alt="poster-img">
                    <!-- :hover features -->
                    <div class="features">
                        <h4 class="features-title">
                            Illustrations of novel   
                        </h4>
                        <!-- text -->
                        <div class="features-illustration text">
                            <p class="italic">
                                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                            </p>
                        </div>
                    </div>
                    <!-- hover icons -->
                    <div class="shop-icons">
                        <!-- whish -->
                        <div class="whishes-square flex">
                             <img class="whishes" src="../assets/svg/svg-4.svg" alt="whishes-logo">
                        </div>
                        <!-- cart -->
                        <div class="cart-square flex">
                             <img class="cart" src="../assets/svg/svg-6.svg" alt="cart-logo">
                        </div>
                    </div>

                </li>
            </ul>
        </div> 
</template>

<script>
export default {
    name:'SectionTwo',
    // importo l'array tramite props da MainComponent
    props:{
        arrayImg: Array
    },

}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.section-two-container{
    padding: $padding_section;
    
    & .list-second-section.flex{
        flex-wrap: wrap;

        & .item-second-section{
            width: calc(100% / 3);
            position:relative;
            & .features{
                width: 35%;
                position: absolute;
                top: 240px;
                background-color: white;
                display: none;

                & .features-title{
                    font-size: 18px;
                }

                & .features-illustration.text{
                    font-size: 12px;
                }
            }

            & .shop-icons{
                text-align: right;
                position: absolute;
                right: 0;
                top: 100px;
                display: none;
                & .whishes-square.flex{
                    width: 30px;
                    height: 30px;
                    background-color: #ef2853;
                    justify-content: center;
                    align-items: center;
                }
                & .whishes {
                    width: 20px;
                    cursor: pointer;
                }

                & .cart-square.flex{
                    width: 30px;
                    height: 30px;
                    background-color: white;
                    justify-content: center;
                    align-items: center;
                    margin-top: 10px;

                    & .cart {
                        width: 20px;
                        cursor: pointer;  
                    }
                }
            }

            // hover
            &:hover .features{
                display: block;
            }

            &:hover .shop-icons{
                display: block;
            }
        }
    }
}
</style>