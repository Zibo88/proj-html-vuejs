<template>
   <div>
       <SectionOneComponent/>
   </div>
</template>

<script>

import SectionOneComponent from './SectionOneComponent.vue'

export default {
    name:'MainComponent',
    components:{
        SectionOneComponent
    }
  
}
</script>

<style lang="scss" scoped>
@import '../style/common';
@import '../style/variables';

</style>