<template>
    <footer>
        <UpperFooter />
        <LowerFooter />
    </footer>
</template>

<script>
import UpperFooter from './UpperFooter.vue'
import LowerFooter from './LowerFooter.vue'

export default {
    name: 'Footer',
    components: {
        UpperFooter,
        LowerFooter
    },
    data: function(){
        return {

        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/mixins.scss';

    footer{
        height: 50vh;
    }

</style>