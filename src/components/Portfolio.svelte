<script>
  // your script goes here
</script>

<style lang="scss">
  .wrapper {
    padding-top: 30px;
    background-color: white;
    text-align: center;
    h2 {
      color: grey;
    }
  }
  .img-wrapper {
    margin: 10px 0px;
    width: 100%;
    height: auto;
    img {
      width: 100%;
      height: 100%;
    }
  }
  @media (min-width: 960px) {
    .wrapper {
      padding: 30px 0px;
    }
    .layout-wrapper {
      max-width: 960px;
      margin: 0 auto;
      padding-bottom: 20px;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-gap: 20px;
      .img-wrapper {
        margin: 0;
      }
      .i1 {
        grid-column: 1/3;
      }
      .i2 {
        img {
          object-fit: cover;
        }
      }
    }
  }
</style>

<div class="wrapper">
  <h1>Portfolio</h1>
  <h2>Our Work</h2>

  <div class="layout-wrapper">
    <div class="img-wrapper i1">
      <img src="assets/laptop1.jpg" alt="laptop one" />
    </div>
    <div class="img-wrapper i2">
      <img src="assets/phone1.jpg" alt="phone one" />
    </div>
    <div class="img-wrapper i3">
      <img src="assets/laptop2.jpg" alt="laptop two" />
    </div>
    <div class="img-wrapper  i4">
      <img src="assets/phone2.jpg" alt="phone two" />
    </div>
    <div class="img-wrapper i5">
      <img src="assets/phone3.jpg" alt="phone three" />
    </div>
  </div>
</div>
