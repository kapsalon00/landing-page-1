<script>
  import TiSocialFacebookCircular from "svelte-icons/ti/TiSocialFacebookCircular.svelte";
  import TiSocialTwitter from "svelte-icons/ti/TiSocialTwitter.svelte";
  import TiSocialGithub from "svelte-icons/ti/TiSocialGithub.svelte";
  import TiSocialGooglePlusCircular from "svelte-icons/ti/TiSocialGooglePlusCircular.svelte";
  let name, email, message;
  const handleSubmit = () => {
    alert(name + " " + email + " " + message);
    name = "";
    email = "";
    message = "";
  };
</script>

<style lang="scss">
  .wrapper {
    background-color: #f5f5f5;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    h2 {
      color: grey;
      margin: 0px 0px 40px 0px;
    }
    form {
      margin-top: 20px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100%;
      input {
        width: 80%;
      }
      textarea {
        width: 80%;
        resize: none;
      }
    }
  }
  button {
    height: 50px;
    width: 200px;
    background-color: orange;
    color: white;
    border: none;
    border-radius: 5px;
  }
  .info {
    color: grey;
    margin: 50px 10px;
    h2 {
      color: black;
    }
    div {
      margin-top: 50px;
    }
  }
  .icons {
    display: flex;
    div {
      cursor: pointer;

      &:hover {
        color: orange;
      }
    }
  }
</style>

<div class="wrapper">
  <h1>Contact</h1>
  <h2>Get in touch!</h2>
  <form on:submit|preventDefault={handleSubmit}>
    <input bind:value={name} placeholder="Name" type="text" />
    <input bind:value={email} placeholder="E-mail" type="text" />
    <textarea bind:value={message} placeholder="Message" rows="4" type="text" />
    <button>Send a message</button>
  </form>
  <div class="info">
    <h2>Our company</h2>
    <h3>55 Random City</h3>
    <h3>1234 Some Street in City Name</h3>
    <div>
      <h3>tel. 123123123</h3>
      <h3>Cotact@companyname.com</h3>
      <div class="icons">
        <div>
          <TiSocialFacebookCircular />
        </div>
        <div>
          <TiSocialTwitter />
        </div>
        <div>
          <TiSocialGithub />
        </div>
        <div>
          <TiSocialGooglePlusCircular />
        </div>
      </div>
    </div>
  </div>
</div>
