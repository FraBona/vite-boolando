<script >
  import PageHeader from './components/PageHeader.vue';
  import PageMain from './components/PageMain.vue'; 

  export default{
    components: {
      Header: PageHeader,
      Main: PageMain,
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
</template>

<style lang="scss">
@use './style/general.scss';
</style>
