<script>

  export default{
    props: {
      item: Object,
    },
    data() {
      return {};
    },
    mounted() {

    }
  }
</script>

<template>
  <div class="col-4">
    <div class="card">
      <figure class="card__image">
        <img :src="'/img/img/'+item.frontImage" alt="" class="img-person">
        <img :src="'/img/img/'+item.backImage" alt="" class="top-img">
        <span class="heart-icon">&hearts;</span>
        <span class="discount" v-for="tipo in item.badges" :class="{
          'active' : tipo.type === 'discount'
        }">{{ tipo.value }}</span>
        <span class="green-rectangle" v-for="tipo in item.badges" :class="{
          'active' : tipo.type === 'tag'
        }">{{ tipo.value }}</span>
      </figure>
      <div>
      <p class="marca">{{ item.brand }}</p>
      <h5>{{ item.name }}</h5>
      <span class="prezzo">{{ item.price }} &euro;</span>
      <span class="line-through">{{ item.price }} &euro;</span>
      </div>
    </div>
  </div>
</template>

<style scoped>

  .card{
    padding: 40px 10px;
  }

  .img-person{
    width: 100%;
  }

  figure > img{
    display: block;
    width: 100%;

  }

  .card__image{
    position: relative;
  }

  .heart-icon{
    display: inline-block;
    text-align: center;
    width: 50px;
    background-color: rgb(255, 255, 255);
    position: absolute;
    top: 5px;
    right: 0px;
    aspect-ratio: 1/1;
    line-height: 3.5em;
  }

  .discount
  {
    display: inline-block;
    text-align: center;
    width: 50px;
    background-color: rgb(255, 0, 0);
    color: white;
    padding: 3px;
    position: absolute;
    bottom: 35px;
    display: none;
  }

  .green-rectangle{
    display: inline-block;
    text-align: center;
    width: 100px;
    background-color: rgb(0, 128, 0);
    color: white;
    padding: 3px;
    position: absolute;
    bottom: 35px;
    left: 55px;
    display: none;
  }

  .top-img{
    position: absolute;
    left: 0;
    top: 0;
    opacity: 0;
  }

  .card:hover .top-img{
    opacity: 1;
  }

  .prezzo{
    color: red;
    font-size: 15px;
  }

  .line-through{
    text-decoration: line-through;
    font-size: 10px;
  }

  .marca{
    color: grey;
  }

  .active{
    display: block;
  }
</style>