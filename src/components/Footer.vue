<template>
    <footer>
        <UpperFooter />
        <LowerFooter />
    </footer>
</template>

<script>
import UpperFooter from './UpperFooter.vue'
import LowerFooter from './LowerFooter.vue'

export default {
    name: 'Footer',
    components: {
        UpperFooter,
        LowerFooter
    }
}
</script>

<style lang="scss" scoped>

</style>