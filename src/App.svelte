<script>
  import TopSection from "./components/TopSection.svelte";
  import About from "./components/About.svelte";
  import Services from "./components/Services.svelte";
  import Portfolio from "./components/Portfolio.svelte";
  import Team from "./components/Team.svelte";
  import Sellout from "./components/Sellout.svelte";
  import Contact from "./components/Contact.svelte";
  import Footer from "./components/Footer.svelte";
  import FaArrowAltCircleUp from "svelte-icons/fa/FaArrowAltCircleUp.svelte";
</script>

<style lang="scss">
  .up {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    position: fixed;
    left: 84%;
    top: 92%;
    color: orange;
    cursor: pointer;
    &:hover {
      color: crimson;
    }
  }

  @media (min-width: 700px) {
    .up {
      left: 92%;
      top: 92%;
    }
  }
</style>

<main>
  <div
    class="up"
    on:click={() => {
      window.scrollTo({ top: 0, behavior: 'smooth' });
    }}>
    <FaArrowAltCircleUp />
  </div>
  <TopSection />
  <div id="about">
    <About />
  </div>
  <div id="services">
    <Services />
  </div>
  <div id="portfolio">
    <Portfolio />
  </div>
  <div id="team">
    <Team />
  </div>
  <Sellout />
  <div id="contact">
    <Contact />
  </div>
  <Footer />
</main>
