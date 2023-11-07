<script >
  import PageHeader from './components/PageHeader.vue';
  import PageFooter from './components/PageFooter.vue'; 
  import Card from './components/Card.vue'; 

  export default{
    components: {
      Header: PageHeader,
      Footer: PageFooter,
      Card: Card,
    },
    data(){
      return{

      }
    }
  }
</script>

<template>
  <Header></Header>
  <main>
    <div class="section">
      <div class="container">
        <div class="row">
          <div class="col-4" v-for="(card ) in 6">
            <Card></Card>
          </div>
        </div>
      </div>
    </div>
  </main>
  <Footer></Footer>
</template>

<style lang="scss">
@use './style/general.scss';
</style>
