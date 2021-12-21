<template>
    <section class="single_series_wrapper p_10">
        <div class="thumb_wrapper w_200p h_200p">
            <img :src="seriesObject.thumb" :alt="'Immagine di ' + seriesObject.series">
        </div>
        <h3 class="mt_10 fs_15">{{seriesObject.series}}</h3>
    </section>
</template>

<script>
export default {
    name: 'SingleSeries',
    props: ['seriesObject']
}
</script>

<style lang="scss" scoped>
    .single_series_wrapper{
        width: calc(100% / 6);
        text-transform: uppercase;
        color: white;

        .thumb_wrapper{
            overflow: hidden;

            img{
                width: 100%;
                height: 150%;
                object-fit: cover;
            }
        }
    }
</style>