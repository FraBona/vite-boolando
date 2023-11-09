<script >
  import PageHeader from './components/PageHeader.vue';
  import PageFooter from './components/PageFooter.vue'; 
  import Card from './components/Card.vue'; 
  //import db from '../db.json';
  import axios from 'axios';
  import { store } from './store';
  export default{
    components: {
      Header: PageHeader, 
      Footer: PageFooter,
      Card: Card,
    },
    data(){
      return{
        store: store,
        openModal: false,
        selectCard: {}
      }
    },
    methods: {
      showModal(item){
        console.log(item);
        this.openModal = true;
        this.selectCard = item;
      },
      closeModal(){
        this.openModal = false;
      }
    },  
    mounted() {
      console.log(this.store);
    },
    created(){
      axios.get('http://localhost:3000/products')
      .then(res =>{
        const cardStore = res.data;
        this.store.cardStore = cardStore
        console.log(cardStore);
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
          <Card v-for="product in store.cardStore" :item="product" @show="showModal"></Card>
        </div>
      </div>
    </div>
  </main>
  <div v-if="openModal" class="modal">
    <div class="content">
      <div class="content_header">
        <span>{{ selectCard.brand }}</span>
        <span class="close" @click="closeModal()">X</span>
      </div>
      <div class="content_body">
          <p>{{selectCard.name}}</p>
          <p>{{ selectCard.price }}</p>
      </div>
    </div>
  </div>
  <Footer></Footer>
</template>

<style lang="scss">
@use './style/general.scss';

.modal::after{
  content: '';
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  z-index: 40;
  background-color: rgba(0,0,0, 0.5);
}

.modal .content{
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, 50%);
  z-index: 50;
  background-color: white;
  border-radius: 20px;
  padding: 20px;
  width: 100%;
  max-width: 500px;
  box-shadow: 0px 0px 20px rgba(0, 0, 0, 0.2);
}

.content_header{
  display: flex;
  justify-content: space-between;
  align-items: center;
}

</style>
