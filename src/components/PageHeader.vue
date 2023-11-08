<script setup>

</script>

<template>
 <header class="page-header">
    <div class="container header-container">
      <div class="row justify-between">
        <div class="col">
          <ul class="menu">
            <li class="menu__items"><a href="">Donna</a></li>
            <li class="menu__items"><a href="">Uomo</a></li>
            <li class="menu__items"><a href="">Bambini</a></li>
          </ul>
        </div>
        <div class="col">
          <img src="/img/img/boolean-logo.png" alt="" class="logo">
        </div>
        <div class="col">
          <img src="/img/img/login.png" alt="" class="icon-header">
          <img src="/img/img/heart.png" alt="" class="icon-header">
          <img src="/img/img/shop.png" alt="" class="icon-header">
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
  .page-header{
    width: 100%;
    position: fixed;
    top: 0px;
    background-color: rgb(255, 105, 0);
    padding: 25px 0px;
    z-index: 1;
  }

  .menu a{
    color: white;
    text-decoration: none;
    padding: 0px 10px;
  }
  .menu a:visited{
    text-decoration: none;
  }
  .menu__items{
    font-size: 18px;
  }
  .logo{
    width: 150px;
  }
  .icon-header{
    width: 20px;
  }
</style>
