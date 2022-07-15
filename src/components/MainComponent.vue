<template>
    <div class="main-container">
        <section class="section-one-container flex">
            <!-- arrow left -->
            <div class="square-carosell flex">
                <img class="arrow left" src="../assets/svg/svg-2.svg" alt="arrow-left-icon">
            </div>
           <!-- section one -->
            <div class="section-one-container flex">
                <!-- column left -->
                <div class="col-left">
                    <!-- titolo-->
                    <h2>
                        Devotion that never <em>end</em>
                    </h2>
                    <!-- testo -->
                    <p class="text">
                        Lorem ipsum dolor sit amet consectetur adipisicing elit. Autem placeat a maiores eius, accusantium nulla suscipit dolore natus numquam,
                    </p>
                    <button>READ MORE</button>
                </div>
                <!-- column right -->
                <div class="col-right flex">
                   <div class="sub-clmn-left">
                      <img src="../assets/img/h-2-slider-img-15.png" alt="">
                      <img class="leaf" src="../assets/img/h-2-slider-img-12.png" alt="">
                   </div>
                   <div class="sub- column-right">
                      <img src="../assets/img/h-2-slider-img-16.png" alt="">
                   </div>
                </div>
            </div>
            <!-- arrow right -->
            <div class="square-carosell flex">
                <img class="arrow right" src="../assets/svg/svg-2.svg" alt="arrow-right-icon">
            </div> 
        </section>
         <!-- <div class="svg-test">
            <img src="../assets/svg/svg-7.svg" alt="">
        </div> -->
    </div>
</template>

<script>
export default {
    name:'MainComponent'
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
    // test
    background-color: pink;
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
}

.left{
    transform: rotate(270deg);
}

.right{
    transform: rotate(90deg);
}

.svg-test{
    background-color: lightcoral;
}

.section-one-container.flex{
    padding: 20px 0;
    justify-content: space-between;

    & .col-left{
        width: 30%;
        margin-left: 15%;
        & h2{
            font-size: 55px;
        }

        & .text{
            padding: 25px 0;
        }

        & button{
            padding: 22px;
            border: 4px solid $utility_color;
            font-size: 12px;
        }
    }

    & .col-right{
        width: 60%;
        padding-left: 25px;

        .sub-clmn-left{
            position: relative;
            & .leaf{
                width: 30px;
                position: absolute;
                top:200px;
                left: 0;
            }
        }
    }

}

</style>