<script>
  import Navbar from '../components/Navbar.svelte';
  import Hero from '../components/Hero.svelte';
  import Stats from '../components/Stats.svelte';
  import About from '../components/About.svelte';
  import Cards from '../components/Cards.svelte';
  import Testimonials from '../components/Testimonials.svelte';
  import Footer from '../components/Footer.svelte';
  import Suscribe from '../components/Suscribe.svelte';
  import { Page } from "framework7-svelte";


</script>

<Page name="home">

  <Navbar />
  <Hero />
  <Stats />
  <About />
  <Cards />
  <Testimonials />
  <Suscribe />
  <Footer />

</Page>
