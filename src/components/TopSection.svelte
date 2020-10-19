<script>
  let src = "assets/bgc.jpg";
</script>

<style lang="scss">
  .image {
    width: 100%;
    height: 100%;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    filter: grayscale(0%);
  }

  .nav-wrapper {
    padding: 10px 10px 0px 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    .dark-bgc {
      background-color: black;
      padding: 10px;
      h1 {
        color: white;
        margin: 2px;
        font-size: 20px;
      }
    }

    .hamburger {
      width: 40px;
      height: 40px;
      padding: 5px;
      border: 1px solid orange;
      border-radius: 2px;
      div {
        width: 35px;
        height: 5px;
        background-color: orange;
        margin: 6px auto;
      }
    }
  }
  .things {
    margin-top: 50px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    .dark {
      background-color: black;
      padding: 10px;
      margin: 5px;
      h1,
      h2 {
        margin: 5px 5px;
        color: white;
        text-align: center;
      }
    }
    button {
      margin: 50px 0px;
      height: 50px;
      width: 200px;
      background-color: orange;
      color: white;
      border: none;
      border-radius: 5px;
    }
  }
</style>

<div class="image" style="background: url('{src}') no-repeat center center">
  <div class="nav-wrapper">
    <div class="dark-bgc">
      <h1>Landing Page</h1>
    </div>
    <div class="hamburger">
      <div />
      <div />
      <div />
    </div>
  </div>
  <div class="things">
    <div class="dark">
      <h1>Lorem ipsum dolor</h1>
    </div>
    <div class="dark">
      <h2>Just for you</h2>
    </div>
    <button>Download Now</button>
  </div>
</div>
