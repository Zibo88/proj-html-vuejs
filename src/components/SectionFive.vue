<template>
    <div class="section-5-container flex">
        <!-- esegu un ciclo v-for per ogni elemento in props blogImg -->
        <div v-for="element, index in blogImg" :key="index" class="card">
            <!-- img -->
            <img class="blog-img" :src="require(`../assets/img/${element.img}`)" alt="blog-img">
            <!-- title -->
            <h4 class="title-card light-weight">{{element.title}}</h4>
            <!-- author -->
            <div class="author italic">{{element.author}}</div>
            <!-- date -->
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
    // importo l'array blogImg da Maincomponent
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