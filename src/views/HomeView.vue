<template>
  <div class="home">
    <img alt="Zid logo" src="../assets/zid-logo.png">
    <WelcomePage msg="Welcome to the Zid Challenge!"/>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component';
import WelcomePage from '@/components/WelcomePage.vue';

@Options({
  components: {
    WelcomePage,
  },
})
export default class HomeView extends Vue {}
</script>

<style scoped>
img {
  margin: 30px 0 0;
}
</style>
