<template>
  <div class="home">
    <div class="wow heartBeat" data-wow-duration="1.5s">
      <img alt="Vue logo" src="../assets/logo.png">

    </div>

    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import {WOW} from '../../node_modules/wowjs/dist/wow';

export default {
  name: 'home',
  mounted(){
    let wow = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: true
    });
    wow.init();
  },
  components: {
    HelloWorld
  }
}
</script>
<style lang="stylus">
  .home
    padding-top 120px
</style>
