<script >

</script>

<template> 
  <main class="page-content">
    <section>
      <div class="container">
        <div class="row">
          <div class="col-4">
            <div class="card">
              <figure class="card__image">
                <img src="../img/img/1.webp" alt="" class="img-person">
                <img src="../img/img/1b.webp" alt="" class="top-img">
                <span class="heart-icon">&hearts;</span>
                <span class="discount">-50%</span>
                <span class="green-rectangle">sostenibilita</span>
              </figure>
              <div>
                <p class="marca">levis</p>
                <h5>RELAXED FIT TEE UNISEX</h5>
                <span class="prezzo">14,99 &euro;</span>
                <span class="line-through">29,99 &euro;</span>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <figure class="card__image">
                <img src="../img/img/2.webp" alt="" class="img-person">
                <img src="../img/img/2b.webp" alt="" class="top-img">
                <span class="heart-icon">&hearts;</span>
                <span class="discount">50%</span>
              </figure>
              <div>
                <p class="marca">levis</p>
                <h5>RELAXED FIT TEE UNISEX</h5>
                <span class="prezzo">14,99 &euro;</span>
                <span class="line-through">29,99 &euro;</span>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <figure class="card__image">
                <img src="../img/img/3.webp" alt="" class="img-person">
                <img src="../img/img/3b.webp" alt="" class="top-img">
                <span class="heart-icon">&hearts;</span>
                <span class="discount">-50%</span>
              </figure>
              <div>
                <p class="marca">levis</p>
                <h5>RELAXED FIT TEE UNISEX</h5>
                <span class="prezzo">14,99 &euro;</span>
                <span class="line-through">29,99 &euro;</span>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <figure class="card__image">
                <img src="../img/img/4.webp" alt="" class="img-person">
                <img src="../img/img/4b.webp" alt="" class="top-img">
                <span class="heart-icon">&hearts;</span>
                <span class="discount">-50%</span>
                <span class="green-rectangle">sostenibilita</span>
              </figure>
              <div>
                <p class="marca">levis</p>
                <h5>RELAXED FIT TEE UNISEX</h5>
                <span class="prezzo">14,99 &euro;</span>
                <span class="line-through">29,99 &euro;</span>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <figure class="card__image">
                <img src="../img/img/5.webp" alt="" class="img-person">
                <img src="../img/img/5b.webp" alt="" class="top-img">
                <span class="heart-icon">&hearts;</span>
                <span class="discount">-50%</span>
              </figure>
              <div>
                <p class="marca">levis</p>
                <h5>RELAXED FIT TEE UNISEX</h5>
                <span class="prezzo">14,99 &euro;</span>
                <span class="line-through">29,99 &euro;</span>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="card">
              <figure class="card__image">
                <img src="../img/img/6.webp" alt="" class="img-person">
                <img src="../img/img/6b.webp" alt="" class="top-img">
                <span class="heart-icon">&hearts;</span>
                <span class="discount">-50%</span>
                <span class="green-rectangle">sostenibilita</span>
              </figure>
              <div>
                <p class="marca">levis</p>
                <h5>RELAXED FIT TEE UNISEX</h5>
                <span class="prezzo">14,99 &euro;</span>
                <span class="line-through">29,99 &euro;</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

</template>

<style scoped>
  main{
    margin: 100px 0;
  }

  .page-content{
    padding: 50px 0px;
  }

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
</style>
