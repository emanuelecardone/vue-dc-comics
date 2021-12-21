<template>
    <main>
        <div class="banner_section w_100"></div>
        <CurrentSeries />
        <PreFooter />
    </main>
</template>

<script>
import CurrentSeries from './CurrentSeries.vue';
import PreFooter from './PreFooter.vue';

export default {
    name: 'Main',
    components: {
        CurrentSeries,
        PreFooter
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/mixins.scss';

    main{
        
        .banner_section{
            height: $banner_height;
            background-image: url('../assets/img/jumbotron.jpg');
            @include common_bg;
            background-position: top;
        }
    }
    
    

</style>