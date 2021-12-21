<template>
    <main>
        <div class="empty_content_section w_100 h_40">
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
@import '../style/variables.scss';

    main{
        
        .empty_content_section{
            background-color: #1c1c1c;
            display: flex;
            align-items: center;

            h2{
                color: white;
                font-size: 27.5px;
            }
        }
    }
    
    

</style>