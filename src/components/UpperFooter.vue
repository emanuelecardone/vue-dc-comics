<template>
    <section class="upper_footer_wrapper">
        <div class="my_container h_100 d_flex justify_content_between">
            <div class="upper_footer_subwrapper left w_40 h_100 d_flex flex_column flex_wrap">
                <!-- La classe dinamica ha il senso di settare height 100% solo per le liste 3 e 4, in modo da settare 65 35 per le prime 2 e,
                 col flex column e wrap, far si che solo le prime 2 stiano nella stessa col -->
                <div v-for="(list, listIndex) in footerLists" :key="listIndex" class="footer_list_wrapper" :class="{'h_65': listIndex === 0, 'h_35': listIndex === 1, 'h_100': listIndex > 1}">
                    <div v-if="footerLists.length > 0" class="footer_list_subwrapper">
                        <h2 class="mb_20">{{list.title}}</h2>
                        <ul>
                            <li v-for="(link, linkIndex) in footerLists[listIndex].links" :key="linkIndex">
                                <a @click.prevent :href="link.url">{{link.name}}</a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="upper_footer_subwrapper right w_40 h_100">
                
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'UpperFooter',
    data: function(){
        return {
            numberOfCols: 3,
            footerLists: [
                {
                    title: 'dc comics',
                    links: [
                        {
                            name: 'Characters',
                            url: '#'
                        },
                        {
                            name: 'Comics',
                            url: '#'
                        },
                        {
                            name: 'Movies',
                            url: '#'
                        },
                        {
                            name: 'TV',
                            url: '#'
                        },
                        {
                            name: 'Games',
                            url: '#'
                        },
                        {
                            name: 'Videos',
                            url: '#'
                        },
                        {
                            name: 'News',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'shop',
                    links: [
                        {
                            name: 'Shop DC',
                            url: '#'
                        },
                        {
                            name: 'Shop DC Collectibles',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'dc',
                    links: [
                        {
                            name: 'Terms Of Use',
                            url: '#'
                        },
                        {
                            name: 'Privacy policy (New)',
                            url: '#'
                        },
                        {
                            name: 'Ad Choices',
                            url: '#'
                        },
                        {
                            name: 'Advertising',
                            url: '#'
                        },
                        {
                            name: 'Jobs',
                            url: '#'
                        },
                        {
                            name: 'Subscriptions',
                            url: '#'
                        },
                        {
                            name: 'Talent Workshops',
                            url: '#'
                        },
                        {
                            name: 'CPSC Certificates',
                            url: '#'
                        },
                        {
                            name: 'Ratings',
                            url: '#'
                        },
                        {
                            name: 'Shop Help',
                            url: '#'
                        },
                        {
                            name: 'Contact Us',
                            url: '#'
                        }
                    ]
                },
                {
                    title: 'sites',
                    links: [
                        {
                            name: 'DC',
                            url: '#'
                        },
                        {
                            name: 'MAD Magazine',
                            url: '#'
                        },
                        {
                            name: 'DC Kids',
                            url: '#'
                        },
                        {
                            name: 'DC Universe',
                            url: '#'
                        },
                        {
                            name: 'DC Power Visa',
                            url: '#'
                        }
                    ]
                },
            ]
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/mixins.scss';

    .upper_footer_wrapper{
        height: $banner_height;
        background-image: url('../assets/img/footer-bg.jpg');
        @include common_bg;
        background-position: top;
        .my_container{

            .upper_footer_subwrapper{

                &.left{
                    padding: 3rem 0;

                    .footer_list_wrapper{

                        h2{
                            color: white;
                            text-transform: uppercase;
                        }
                        a{
                            color: $secondary_color;
                            line-height: 22.5px;
                        }
                    }   
                }
                &.right{
                    background-image: url('../assets/img/dc-logo-bg.png');
                    @include common_bg;
                    background-position: center;
                }
            }
        }

    }

</style>