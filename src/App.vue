<template>
  <div id="app">
    <header>
      <Header />
      <HeaderHero />
    </header>

    <footer>
      <FooterTop class="footer_top"/>
      <FooterBottom />
    </footer>
  </div>
    
</template>

<script>
import Header from '@/components/Header.vue';
import HeaderHero from '@/components/HeaderHero.vue';
import FooterTop from '@/components/FooterTop.vue';
import FooterBottom from '@/components/FooterBottom.vue';

export default {
  name: 'App',
  components: {
    Header,
    HeaderHero,
    FooterTop,
    FooterBottom
  }
}
</script>

<style lang="scss">
*{
  font-family: Avenir, Helvetica, Arial, sans-serif;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  height: 100vh;
}
#app{
  height: 100%;
  display: flex;
  flex-direction: column;
  min-width: 2000px;
}
footer{
  height: 100%;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
  
  .footer_top{
    flex-grow: 1;
  }

}

</style>
