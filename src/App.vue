<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue"

export default {
  name: "App",
  components: {
    Header,
    Main
  },
};
</script>

<style lang="scss">
@import './style/variables.scss';
@import './style/mixins.scss';
@import './style/general.scss';
@import './style/utilities.scss';

/* Sto facendo si che tutti i div con classe my_container abbiano massimo 1400px di width */
.my_container{
  @include common_container;
}

</style>
