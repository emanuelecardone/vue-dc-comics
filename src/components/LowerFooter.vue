<template>
    <div class="lower_footer_wrapper w_100 d_flex align_items_center">
        <div class="my_container">
            <a @click.prevent class="sign_up" href="#">sign-up now!</a>
            <div class="lower_footer_right d_flex align_items_center">
                <h2 class="me_35">follow us</h2>
                <ul v-if="linksList.length > 0">
                    <li v-for="(link, linkIndex) in linksList" :key="linkIndex">
                        <a @click.prevent :href="link.url">
                            <img :src="require('../assets/img/footer-' + link.img + '.png')" :alt="'Logo di ' + link.img">
                        </a>
                    </li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'LowerFooter',
    data: function(){
        return {
            linksList: [
                {
                    img: 'facebook',
                    url: '#'
                },
                {
                    img: 'twitter',
                    url: '#'
                },
                {
                    img: 'youtube',
                    url: '#'
                },
                {
                    img: 'pinterest',
                    url: '#'
                },
                {
                    img: 'periscope',
                    url: '#'
                }
            ]
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/mixins.scss';

    .lower_footer_wrapper{
        text-transform: uppercase;
        height: $head_foot_height;
        background-color: $tertiary_color;

        .my_container{
            @include between_spacing;

            a{
                padding: 1rem;
                border: 2px solid $primary_color;
                color: white;
            }
            .lower_footer_right{
                
                h2{
                    color: $primary_color;
                }
                ul{
                    @include inline_ul;
                    gap: 15px;
                }
                a{  
                    padding: 0;
                    border: none;
                }
            }
        }
    }
</style>