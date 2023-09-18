<script>
  import { Block } from "framework7-svelte";

  let src = "/images/disco.jpg";
</script>

<Block>
  <div class="hero-container">
    <div class="text-container">
      <h1 class="hero-h1">Tu boleto hacia noches inolvidables</h1>
      <p class="hero-p">
        Tu acceso sin complicaciones a la mejor vida nocturna en Argentina.
        Simplificamos tus noches para que sean inolvidables.
      </p>
    </div>
    <div class="img-container">
      <img {src} alt="banner" class="hero-img" />
    </div>
  </div>
</Block>
