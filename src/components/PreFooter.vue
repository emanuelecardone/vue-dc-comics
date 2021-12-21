<template>
    <section class="prefooter_section">
        <div class="my_container">
            <ul v-if="prefooterLinks.length > 0">
                <li v-for="(link, index) in prefooterLinks" :key="index">
                    <img :src="require('../assets/img/' + link.img)" :alt="'Immagine di' + link.text">
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
        width: 100%;
        height: 60%;
        display: flex;
        align-items: center;
        background-color: lighten($primary_color, 10%);

        ul{
            @include inline_ul;
            padding: 0 30px;
            
            li{
                display: flex;
                justify-content: space-between;
                align-items: center;
                gap: 15px;

                img{
                    width: 45px;
                }
                a{
                    color: white;
                }
            }
        }
    }
</style>