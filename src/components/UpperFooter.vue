<template>
    <section class="upper_footer_wrapper">
        <div class="my_container">
            <div class="upper_footer_subwrapper left">
                test
            </div>
            <div class="upper_footer_subwrapper right">
                test
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'UpperFooter'
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/mixins.scss';

    .upper_footer_wrapper{
        height: $middle_height;
        background-image: url('../assets/img/footer-bg.jpg');
        @include common_bg;
        background-position: top;
        .my_container{
            height: 100%;
            display: flex;

            .upper_footer_subwrapper{
                width: 50%;
                height: 100%;

                &.right{
                    background-image: url('../assets/img/dc-logo-bg.png');
                    @include common_bg;
                    background-position: center;
                }
            }
        }

    }

</style>