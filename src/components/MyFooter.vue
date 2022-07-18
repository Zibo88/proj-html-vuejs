<template>
    <div class="footer-container">
        <ul class="list flex">
            <!-- first elemente -->
            <li class="list-item">
                <!-- img -->
                <img class="footer-item" :src="info.img" alt="footer-logo-img">
                <!-- slogan -->
                <div class="footer-item">
                    {{info.slogan}}
                </div>
            </li>
            <!-- second element -->
            <li class="list-item">
                <!-- email -->
                <div class="footer-item">
                    {{info.email}}
                </div>
                <!-- telephone -->
                <div class="footer-item">
                    {{info.telephone}}
                </div>
            </li>

            <!-- third element -->
            <li class="list-item">
                <!-- address -->
                <div class="footer-item">
                    {{info.address}}
                </div>
                <!-- city -->
                <div class="footer-item">
                    {{info.city}}
                </div>
            </li>

            <li class="list-item">
                <div class="footer-item">
                    {{info.socialTitle}}
                </div>
                <div class="footer-item">

                </div>
            </li>



          
        </ul>
    </div>
</template>

<script>
export default {
    name:'MyFooter',
    props:{
        info:Object
    },
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.footer-container{
    background-color: $color_green;
   
    
    & .list{
         width: 60%;
        margin: 0 auto;

        & .list-item{
        width: calc((100% / 4) - 10px);
        padding: 10px 0;

            & .footer-item{
                padding: 5px 0;
                font-size: 13px;
            }
        }
    }
    
}
</style>