<script >
  import PageHeader from './components/PageHeader.vue';
  import PageMain from './components/PageMain.vue'; 
  import PageFooter from './components/PageFooter.vue'; 

  export default{
    components: {
      Header: PageHeader,
      Main: PageMain,
      Footer: PageFooter
    },
    data(){
      return{

      }
    }
  }
</script>

<template>
  <Header></Header>
  <Main></Main>
  <Footer></Footer>
</template>

<style lang="scss">
@use './style/general.scss';
</style>
