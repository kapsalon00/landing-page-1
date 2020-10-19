<script>
  import DiApple from "svelte-icons/di/DiApple.svelte";
  import DiLinux from "svelte-icons/di/DiLinux.svelte";
  import DiAndroid from "svelte-icons/di/DiAndroid.svelte";
</script>

<style lang="scss">
  .services {
    background-color: #f5f5f5;
    text-align: center;
  }

  .wrapper {
    .service {
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
    }
    .icon-wrapper {
      background-color: white;
      border-radius: 50%;
      width: 105px;
      height: 105px;
      position: relative;
      transition: 0.5s;
      cursor: pointer;
      &:hover {
        background-color: orange;
        .icon {
          color: white;
        }
      }
    }
    .icon {
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      width: 55px;
      height: 55px;
      color: orange;
    }
  }
</style>

<div class="services">
  <h1>Services</h1>
  <p>What we do?.</p>
  <div class="wrapper">
    <div class="service service1">
      <div class="icon-wrapper">
        <div class="icon">
          <DiApple />
        </div>
      </div>
      <h2>IOS Apps</h2>
      <p>
        Vestibulum odio risus, interdum fringilla vulputate ac, placerat in mi.
        Vivamus pharetra, mauris vitae cursus ultricies.
      </p>
    </div>
    <div class="service service2">
      <div class="icon-wrapper">
        <div class="icon">
          <DiLinux />
        </div>
      </div>
      <h2>Linux Apps</h2>
      <p>
        Vestibulum odio risus, interdum fringilla vulputate ac, placerat in mi.
        Vivamus pharetra, mauris vitae cursus ultricies.
      </p>
    </div>
    <div class="service service3">
      <div class="icon-wrapper">
        <div class="icon">
          <DiAndroid />
        </div>
      </div>
      <h2>Android Apps</h2>
      <p>
        Vestibulum odio risus, interdum fringilla vulputate ac, placerat in mi.
        Vivamus pharetra, mauris vitae cursus ultricies.
      </p>
    </div>
  </div>
</div>
