<template>
   <div class="main-container">
        <section class="section-one-container flex">
            <!-- arrow left -->
            <div class="square-carosell flex">
                <img class="arrow left" src="../assets/svg/svg-2.svg" alt="arrow-left-icon">
            </div>
           <!-- section one -->
            <div class="section-one flex">
                <!-- column left -->
                <div class="col-left">
                    <!-- titolo-->
                    <h2>
                        Devotion that never <span class="italic">end</span>
                    </h2>
                    <!-- testo -->
                    <p class="text">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem placeat a maiores eius, accusantium nulla suscipit dolore natus numquam,
                    </p>
                    <button>
                        <a href="#">Read More</a>
                    </button>
                </div>
                <!-- column right -->
                <div class="col-right flex">
                   <div class="sub-clmn-left">
                      <img class="woman" src="../assets/img/h-2-slider-img-15.png" alt="">
                      <img class="leaf" src="../assets/img/h-2-slider-img-12.png" alt="leaf-img">
                      <img class="green-branch" src="../assets/img/h-2-slider-img-13.png" alt="green-branch-img">
                      <img class="pink-butterfly" src="../assets/img/short-slider-rev-1-img-2.png" alt="">
                   </div>
                   <div class="sub-column-right">
                        <img class="man" src="../assets/img/h-2-slider-img-16.png" alt="">
                        <img class="brown-branch" src="../assets/img/h-2-slider-img-14.png" alt="brown-branch">
                        <img class="pink-butterfly-right" src="../assets/img/short-slider-rev-1-img-2.png" alt="pink-burrfly">
                        <img class="leafs" src="../assets/img/h-2-slider-img-17.png" alt="leafs">
                   </div>
                </div>
            </div>
            <!-- arrow right -->
            <div class="square-carosell flex">
                <img class="arrow right" src="../assets/svg/svg-2.svg" alt="arrow-right-icon">
            </div> 
        </section>
        <div class="slider-indicator">
            <i v-for="n in 3" :key="n" class="fa-solid fa-circle"></i>
        </div>
       
    </div>
</template>

<script>
export default {
    name: 'SectionOneComponent'
    
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.section-one-container{
    width: 95%;
    margin: 0 auto;
    align-items: center;
    justify-content: space-between;
    padding: 40px 0 20px 0;
    
    & .section-one{
        width: 80%;
        padding: 60px 0 20px 0;

         & .col-left{
        width: 40%;
        margin-left: 15%;
        & h2{
            font-size: 55px;
        }

        & .text{
            padding: 25px 0;
        }

        & button{
            padding: 15px 30px;
            border: 4px solid $utility_color;
            font-size: 14px;
            & a{
                color: black;
            }
            
            &:hover{
                background-color: $utility_color;
                border: 4px solid white;

                a{
                    color: white;
                }
            }
        }
    }

    & .col-right{
        width: 60%;
        padding-left: 25px;

        .sub-clmn-left{
            position: relative;
            & .woman{
                width: 100%;
                margin-left: 12px;
            }
            & .man{
                 width: 90%;
             }
            & .leaf{
                width: 25px;
                position: absolute;
                top:155px;
                left: 0;
            }
            & .green-branch{
                width: 40px;
                position: absolute;
                bottom:35px;
                left: 20px;
            }

            & .pink-butterfly{
                width: 40px;
                position: absolute;
                top: 0;
                left: 10px;
            }

        }

        .sub-column-right{
            position: relative;
            & .man{
                width: 100%;
                margin-right: 20px;
            }

            & .brown-branch{
                    width: 50px;
                    position: absolute;
                    right: 48px;
                    top: -53px;
            }

            & .pink-butterfly-right{
                width: 40px;
                position: absolute;
                top: 50px;
                right: 30px;
                transform:rotate(94deg)
            }

             & .leafs{
                width: 60px;
                position: absolute;
                bottom: 35px;
                right: -80px;
            }
        }
    }
    }
}

.square-carosell{
    background-color: $utility_color;
    width: 30px;
    height: 30px;
    border-radius: 50%;
    justify-content: center;
    align-items: center;
    
}

.arrow{
    width: 20px;
    border-radius: 50%;
    padding: 3px;
    cursor: pointer;
}

.left{
    transform: rotate(270deg);
}

.right{
    transform: rotate(90deg);
}

.slider-indicator{
    text-align: center;

    & i{
        padding: 0px 10px;
        color: $utility_color;
    }
}

// test
// .svg-test{
//     background-color: black;
// }
</style>