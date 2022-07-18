<template>
    <div class="section-5-container flex">
        <div v-for="element in blogImg" :key="element" class="card">
            <!-- <img :src="`../assets/img/${element.img}`" alt=""> -->
            <img class="blog-img" src="../assets/img/h-2-blog-img-3.jpg" alt="blog-img">
            <h4 class="title-card light-weight">{{element.title}}</h4>
            <div class="author italic">{{element.author}}</div>

            <div class="date">
                <div class="day italic">{{element.day}}</div>
                <div class="month-and-year">{{element.monthAndYear}}</div>
            </div>  
           
        </div>
    </div>
</template>

<script>
export default {
    name: 'SectionFive',
    props:{
        blogImg:Array
    }
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

.section-5-container.flex{
    width: 60%;
    margin: 0 auto;
    padding: $padding_section;

    & .card {
        margin: 10px;
        width: calc((100% / 3) - 20px);
        position: relative;

        &:hover .blog-img{
            cursor: pointer;
            transform: scale(1.1);
        }

        & h4 {
            padding: 15px 0; 
        }

        & .author {
            font-size: 13px;
        }

        & .date{
            text-align: center;
            width: 15%;
            position: absolute;
            top: -7px;
            left: 8px;

            & .day {
                font-size: 20px;
                background-color: $color_green;
            }

            & .month-and-year{
            font-size: 8px;
            background-color: hsl(11deg 64% 87%);
            padding: 3px;
            font-weight: 600;
            }
        }
       
    }
}


</style>