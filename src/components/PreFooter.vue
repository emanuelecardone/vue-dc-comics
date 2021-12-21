<template>
    <section class="prefooter_section w_100 h_150p d_flex align_items_center">
        <div class="my_container">
            <ul v-if="prefooterLinks.length > 0" class="px_40">
                <li v-for="(link, index) in prefooterLinks" :key="index" class="d_flex justify_content_between align_items_center">
                    <img class="w_50p h_70p" :src="require('../assets/img/' + link.img)" :alt="'Immagine di' + link.text">
                    <a @click.prevent :href="link.url">{{link.text}}</a>
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
                    text: 'digital comics',
                    img: 'buy-comics-digital-comics.png',
                    url: '#'
                },
                {
                    text: 'dc merchandise',
                    img: 'buy-comics-merchandise.png',
                    url: '#'
                },
                {
                    text: 'subscription',
                    img: 'buy-comics-subscriptions.png',
                    url: '#'
                },
                {
                    text: 'comic shop locator',
                    img: 'buy-comics-shop-locator.png',
                    url: '#'
                },
                {
                    text: 'dc power visa',
                    img: 'buy-dc-power-visa.svg',
                    url: '#'
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
        background-color: lighten($primary_color, 10%);

        ul{
            @include inline_ul;
            
            li{
                gap: 15px;

                &:last-child{

                    /* Fix per la svg */
                    img{   
                        transform: scaleX(1.2) scaleY(1.5);
                    }
                }
                a{
                    color: white;
                }
            }
        }
    }
</style>