<script >
  import PageHeader from './components/PageHeader.vue';
  import PageFooter from './components/PageFooter.vue'; 
  import Card from './components/Card.vue'; 
  //import db from '../db.json';
  import { store } from './store';
  import axios from 'axios';
  export default{
    components: {
      Header: PageHeader, 
      Footer: PageFooter,
      Card: Card,
    },
    data(){
      return{
        store: store,
      }
    },
    mounted() {
      console.log(this.store);
    },
    created(){
      axios.get('http://localhost:3000/products')
      .then(res =>{
        console.log(res.data);
      })
    }
  }
</script>

<template>
  <Header></Header>
  <main>
    <div class="section">
      <div class="container">
        <div class="row">
          <Card v-for="product in store.products" :item="product"></Card>
        </div>
      </div>
    </div>
  </main>
  <Footer></Footer>
</template>

<style lang="scss">
@use './style/general.scss';
</style>
