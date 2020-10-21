<script>
  import Modal from "./Modal.svelte";

  let src = "assets/bgc.jpg";
  let pageWidth;

  let showModal = false;
</script>

<style lang="scss">
  .image {
    width: 100%;
    height: 100%;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
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
  .links-wrapper {
    a {
      margin: 0 10px;
      text-decoration: none;
      color: white;
      background-color: black;
      padding: 5px 10px;
      &:hover {
        color: orange;
        cursor: pointer;
      }
    }
  }
  .navs {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    a {
      margin: 10px;
      width: 100px;
      text-align: center;
      font-size: 30px;
      color: grey;
      font-weight: bold;
      cursor: pointer;
      &:hover {
        text-decoration: underline;
      }
    }
  }
  @media (min-width: 960px) {
    .image {
      background-size: cover !important;
    }
    .layout-wrapper {
      max-width: 1080px;
      margin: 0 auto;
    }
  }
</style>

<svelte:window bind:outerWidth={pageWidth} />

<div class="image" style="background: url({src}) no-repeat center center">
  {#if showModal && pageWidth < 960}
    <Modal on:close={() => (showModal = false)}>
      <div class="navs" slot="navs">
        <a on:click={() => (showModal = false)} href="#about">About</a>
        <a on:click={() => (showModal = false)} href="#services">Services</a>
        <a on:click={() => (showModal = false)} href="#portfolio">Portfolio</a>
        <a on:click={() => (showModal = false)} href="#team">Team</a>
        <a on:click={() => (showModal = false)} href="#contact">Contact</a>
      </div>
    </Modal>
  {/if}
  <div class="layout-wrapper">
    <div class="nav-wrapper">
      <div class="dark-bgc">
        <h1>Landing Page</h1>
      </div>
      {#if pageWidth < 960}
        <div
          class="hamburger"
          on:click={() => {
            showModal = true;
          }}>
          <div />
          <div />
          <div />
        </div>
      {:else}
        <div class="links-wrapper">
          <a href="#about">About</a>
          <a href="#services">Services</a>
          <a href="#portfolio">Portfolio</a>
          <a href="#team">Team</a>
          <a href="#contact">Contact</a>
        </div>
      {/if}
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
</div>
