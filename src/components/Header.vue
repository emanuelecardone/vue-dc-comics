<template>
    <header class="w_100">
        <div class="my_container">
            <img class="w_80p" :src="require('../assets/img/' + logoSrc)" alt="Logo DC">

            <ul v-if="headerLinks.length > 0" class="h_100">
                <li v-for="(link, index) in headerLinks" :key="index" class="h_100">
                    <a @click.prevent :href="link.url" class="d_inline_block" :class="{'current': index === currentItem}">{{link.text}}</a> 
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
        
        .my_container{
            @include between_spacing;
        }

        ul{ 
            @include inline_ul;
            gap: 1.5rem;

            li{ 
                height: $head_foot_height;
                a{  
                    color: $tertiary_color;
                    line-height: calc($head_foot_height - 5px);

                    &.current{
                        color: $primary_color;
                        border-bottom: 5px solid $primary_color;
                    }
                
                }
            }
        }
    }

</style>