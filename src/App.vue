<template>
  <div id="app">
    <header>
      <Header />
    </header>

    <main>
      <SectionOne />

    </main>

    <footer>
      <FooterTop class="footer_top"/>
      <FooterBottom />
    </footer>
    

  </div>
    
</template>

<script>
import Header from '@/components/Header.vue';
import SectionOne from '@/components/SectionOne.vue';
import FooterTop from '@/components/FooterTop.vue';
import FooterBottom from '@/components/FooterBottom.vue';

export default {
  name: 'App',
  components: {
    Header,
    SectionOne,
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
