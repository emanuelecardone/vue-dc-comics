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
@import '../style/variables.scss';

    main{
        /* Nell'inspector si vede una linea bianca a fine main che senza inspector non si vede */
        height: $middle_height;
        
        .empty_content_section{
            background-color: $tertiary_color;
            height: 40%;
            width: 100%;
            display: flex;
            align-items: center;

            h2{
                color: white;
                font-size: 27.5px;
            }
        }
    }
    
    

</style>