<template>
    <main>
        <div class="empty_content_section">
            <div class="my_container">
                <h2> {{emptyContentText}} </h2>
            </div>
        </div>
        <PreFooter />
    </main>
</template>

<script>
import PreFooter from './PreFooter.vue'

export default {
    name: 'Main',
    components: {
        PreFooter
    },
    data: function(){
        return {
            emptyContentText: '--> Content goes here <--'
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/mixins.scss';

    main{
        background-color: black;
    }
    .empty_content_section{
        padding: 3rem;
        width: 100%;

        h2{
            color: white;
            font-size: 27.5px;
        }
    }
    

</style>