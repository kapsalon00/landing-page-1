<script>
  // your script goes here
</script>

<style lang="scss">
  .wrapper {
    background-color: #f5f5f5;
    text-align: center;
    padding-top: 30px;
    h2 {
      color: grey;
    }
  }
  .card-wrapper {
    margin-top: 50px;
    img {
      width: 200px;
      height: auto;
    }
    p {
      margin-bottom: 0;
      padding-bottom: 10px;
    }
  }
  @media (min-width:960px){
    .wrapper{
      max-width:960px;
      margin:0 auto;
      padding: 30px;
      
    }
    .cards-layout{
      display:flex;
      .card-wrapper{
      img{
        height:200px;
        object-fit:cover;
      }
      }
    }
  }
</style>

<div class="wrapper">
  <h1>The team</h1>
  <h2>Meet us!</h2>


<div class="cards-layout">
  <div class="card-wrapper">
    <img src="assets/person3.jpg" alt="laptop one" />
    <h1>Steve Regular</h1>
    <p>
      Vestibulum odio risus, interdum fringilla vulputate ac, placerat in mi.
      Vivamus pharetra, mauris vitae cursus ultricies.
    </p>
  </div>
  <div class="card-wrapper">
    <img src="assets/person1.jpg" alt="laptop one" />
    <h1>Erica Regular</h1>
    <p>
      Vestibulum odio risus, interdum fringilla vulputate ac, placerat in mi.
      Vivamus pharetra, mauris vitae cursus ultricies.
    </p>
  </div>
  <div class="card-wrapper">
    <img src="assets/person2.jpg" alt="laptop one" />
    <h1>John Regular</h1>
    <p>
      Vestibulum odio risus, interdum fringilla vulputate ac, placerat in mi.
      Vivamus pharetra, mauris vitae cursus ultricies.
    </p>
  </div>

</div>
</div>