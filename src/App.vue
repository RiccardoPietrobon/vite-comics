<script>

//importo i files che mi servono
import HeaderNav from './components/HeaderNav.vue';
import BlueNav from './components/BlueNav.vue';
import FooterPrincipal from './components/FooterPrincipal.vue';
import SocialFooter from './components/SocialFooter.vue';

export default {
  data() {
    return {
      title: "My app",
    };
  },

  components: { HeaderNav, BlueNav, FooterPrincipal, SocialFooter },
};
</script>

<template>
  <HeaderNav />
  <BlueNav />
  <FooterPrincipal />
  <SocialFooter />
</template>

<style lang="scss">
@use "./assets/scss/general.scss";
</style>
