<template>
    <div class="footer-container">
        <ul class="list flex">

            <!-- first elemente -->
            <li class="list-item">
                <!-- img -->
                <img class="logo" :src="require(`../assets/img/${info.img}`)" alt="footer-logo-img">
                <!-- slogan -->
                <div class="footer-item light-weight">
                    {{info.slogan}}
                </div>
            </li>

            <!-- second element -->
            <li class="list-item">
                <!-- email -->
                <div class="footer-item light-weight">
                    {{info.email}}
                </div>
                <!-- telephone -->
                <div class="footer-item light-weight">
                    {{info.telephone}}
                </div>
            </li>

            <!-- third element -->
            <li class="list-item">
                <!-- address -->
                <div class="footer-item light-weight">
                    {{info.address}}
                </div>
                <!-- city -->
                <div class="footer-item light-weight">
                    {{info.city}}
                </div>
            </li>

            <!-- fourth -->
            <li class="list-item">
                <div class="footer-item">
                    {{info.socialTitle}}
                </div>
                <!-- social link -->
                <div class="social-item-container flex">
                    <!-- eseguo un ciclo v-for dell'array passato tramite props (socialIcon) -->
                    <div class="social-item" v-for="(element, index) in socialIcon" :key="index">  
                        <a class="social-icon" href="#">
                            <i :class="`${element.platform}`"></i>
                        </a> 
                    </div>
                </div>
            </li>

        </ul>
    </div>
</template>

<script>
export default {
    name:'MyFooter',
    // importo l'oggetto relativo alle info da apporre al footer
    // importo l'array contenente le classi che compongono le icone di fontawesome social
    props:{
        info:Object,
        socialIcon:Array,
    },
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.footer-container{
    background-color: $color_green;
    padding: $padding_section;
   
    
    & .list{
         width: 60%;
        margin: 0 auto;
       
        & .list-item{
        width: calc((100% / 4) - 10px);
        padding: 10px 0;

            & .logo{
            width: 100px;
            padding-bottom: 2px;
        }

            & .footer-item{
                padding: 5px 0;
                font-size: 13px;
            }
            & .social-item-container.flex{
                width: 55%;
                justify-content: space-between;

                & .social-item{
                padding-top: 5px;
                font-size: 13px;

                & .social-icon{
                    color: black;
                }
            }
            }
           
        }
    }
    
}
</style>