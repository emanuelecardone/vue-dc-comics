<template>
    <section class="prefooter_section">
        <div class="my_container">
            <ul v-if="prefooterLinks.length > 0">
                <li v-for="(link, index) in prefooterLinks" :key="index">
                    <a href="#">Test</a>
                </li>
            </ul>   
        </div>
    </section>
</template>

<script>
export default {
    name: 'PreFooter',
    data: function(){
        return {
            prefooterLinks: [
                {
                    text: '',
                    img: '',
                    url: ''
                },
                {
                    text: '',
                    img: '',
                    url: ''
                },
                {
                    text: '',
                    img: '',
                    url: ''
                },
                {
                    text: '',
                    img: '',
                    url: ''
                },
                {
                    text: '',
                    img: '',
                    url: ''
                },
            ]
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/mixins.scss';
    
    .prefooter_section{
        width: 100%;
        background-color: $primary_color;
        padding: 4rem;

        ul{
            @include inline_ul;
            
            a{
                color: white;
            }
        }
    }
</style>