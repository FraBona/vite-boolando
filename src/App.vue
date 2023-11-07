<script >
  import PageHeader from './components/PageHeader.vue';
  import PageFooter from './components/PageFooter.vue'; 
  import Card from './components/Card.vue'; 
  import db from './db.json'
  export default{
    components: {
      Header: PageHeader, 
      Footer: PageFooter,
      Card: Card,
    },
    data(){
      return{
        products : db.products,
      }
    },
    mounted() {
      console.log(this.products);
    }
  }
</script>

<template>
  <Header></Header>
  <main>
    <div class="section">
      <div class="container">
        <div class="row">
          <Card v-for="product in products" :item="product"></Card>
        </div>
      </div>
    </div>
  </main>
  <Footer></Footer>
</template>

<style lang="scss">
@use './style/general.scss';
</style>
