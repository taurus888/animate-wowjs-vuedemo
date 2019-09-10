<template>
  <div class="hello">
    <h1 class="wow zoomInUp msg" data-wow-duration="2s" data-wow-delay="0.4s">{{ msg }}</h1>
    <!--<div class="wow bounce ">-->
    <!--　　　　<p>完全契合0基础的学员</p>-->
    <!--　　　　<p>完全契合0基础的学员</p>-->
    <!--</div>-->
    <section class="wow slideInLeft aaa" data-wow-duration="1s">
      <p style="font-size: 26px">
        For a guide and recipes on how to configure / customize this project,<br>
        check out the
        <a href="https://cli.vuejs.org" target="_blank" rel="noopener">vue-cli documentation</a>.
      </p>
      <h3>Installed CLI Plugins</h3>
      <ul>
        <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      </ul>
      <h3>Essential Links</h3>
      <ul>
        <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
        <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
        <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
        <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
        <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
      </ul>
      <h3>Ecosystem</h3>
    </section>
    <section>
      <ul class="lists">
        <li class="wow flipInX" data-wow-duration="1.6s" data-wow-delay="0.8s"><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
        <li class="wow flipInX" data-wow-duration="1.6s" data-wow-delay="0.4s"><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
        <li class="wow jackInTheBox" data-wow-duration="2s"><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
        <li class="wow flipInX" data-wow-duration="1.6s" data-wow-delay="0.4s"><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
        <li class="wow flipInX" data-wow-duration="1.6s" data-wow-delay="0.8s"><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
      </ul>
    </section>

    <div class="box">
      <div class="item">
        <div class="wow fadeInLeftBig one">chapter one</div>
        <div class="wow fadeInRightBig two">chapter two</div>
      </div>
      <div class="item">
        <div class="wow zoomInLeft three">chapter three</div>
        <div class="wow zoomInRight four">chapter four</div>
      </div>
    </div>
    <footer>
      <!--<p class="hel">This is a nice day!I want to go to swimming!</p>-->
      <p class="hel">这里即将展现本页面的所有的目录和链接地址</p>
      <div class="wow fadeInUp" data-wow-duration="1s">
        This is a nice day
      </div>
      <div class="wow fadeInUp" data-wow-duration="1s" data-wow-delay="0.4s">
        This is a nice day This is a nice day
      </div>
      <div class="wow fadeInUp" data-wow-duration="1s" data-wow-delay="0.8s">
        This is a nice day This is a nice day This is a nice day
      </div>
      <div class="wow fadeInUp" data-wow-duration="1s" data-wow-delay="1.2s">
        This is a nice day This is a nice day
      </div>
      <div class="wow fadeInUp" data-wow-duration="1s" data-wow-delay="1.6s">
        This is a nice day This is a nice day
      </div>
    </footer>
  </div>
</template>

<script>
  import WOW from '../../node_modules/wowjs/dist/wow';
   export default {
    name: 'HelloWorld',
    data(){
      return{
        showAni: false
      }
    },
    created(){

    },
    mounted(){
      let wow = new WOW.WOW({
        boxClass: 'wow',
        animateClass: 'animated',
        offset: 0,
        mobile: true,
        live: true
      });
      wow.init();
    },
    props: {
      msg: String
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="stylus">
h3
  margin 40px 0 0

ul
  list-style-type none
  padding 0

li
  display inline-block
  margin 0 10px

a
  color #ffffff

.aaa
  background-color #b6c5ed
  padding 30px 0
  margin-bottom 100px
.lists
  li
    background-color rosybrown
    border-radius 160px
    width 160px
    height 160px
    line-height 160px
  li:nth-child(odd)
    background-color #7497bc
.msg
  padding-bottom 100px
.box
  text-align center
  margin 100px 0
  .item
    display flex
    width 100%
    margin 20px
    font-size 40px
    font-weight bold
    line-height 300px
  .one
    background-color #a4aeb2
    width 40%
    height 300px
  .two
    background-color #b27f94
    width 56%
    height 300px
    margin-left 20px
  .three
    background-color #b1b287
    width 66%
    height 400px
    line-height 400px
  .four
    background-color #988fb2
    width 30%
    height 400px
    line-height 400px
    margin-left 20px
footer
  height 500px
  background-color black
  padding-top 20px
  div
    font-size 30px
    line-height 50px
    color #ffffff
</style>
<style>

  @keyframes typing {
    from { width: 0}
  }
  @keyframes blink-caret {
    50% { border-color: transparent; }
  }
  .hel{
    margin-left: 50px;
    color: #ffffff;
    font: 200% monospace;
    border-right: .08em solid;
    width: 40ch;
    white-space: nowrap;
    overflow: hidden;
    animation: typing 10s steps(20, end),blink-caret .5s step-end infinite alternate;
  }
</style>
