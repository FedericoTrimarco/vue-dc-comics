<template>
  <div id="app">
    <header>
      <Header />
    </header>

    <main>
      <SectionOne />

    </main>
    

  </div>
    
  
</template>

<script>
import Header from '@/components/Header.vue'
import SectionOne from '@/components/SectionOne.vue'

export default {
  name: 'App',
  components: {
    Header,
    SectionOne,
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
</style>
