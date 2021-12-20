<template>
    <header>
        <div class="my_container">
            <img :src="require('../assets/img/' + logoSrc)" alt="Logo DC">

            <ul v-if="headerLinks.length > 0">
                <li v-for="(link, index) in headerLinks" :key="index" :class="{'current': index === currentItem}">
                    <a :href="link.url">{{link.text}}</a> 
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
export default {
    name: 'Header',
    data: function(){
        return {
            logoSrc: 'dc-logo.png',
            currentItem: 1,
            headerLinks: [
                {   
                    text: 'characters',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'comics',
                    current: true,
                    url: '#'
                },
                {   
                    text: 'movies',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'tv',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'games',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'collectibles',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'videos',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'fans',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'news',
                    current: false,
                    url: '#'
                },
                {   
                    text: 'shop',
                    current: false,
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

    header{
        width: 100%;
        height: $head_foot_height;
        
        .my_container{
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        img{
            width: 80px;
        }

        ul{ 
            @include inline_ul;
            gap: 1.5rem;

            li{
                line-height: 115px;
                align-self: flex-start;
                &.current{
                    border-bottom: 5px solid $primary_color;
                    a{
                        color: $primary_color;
                    }
                }

                a{
                    color: $tertiary_color;                    
                }
            }
        }
    }

</style>