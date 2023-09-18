<script>
  const aboutData = {
    companyDescription: `La superapp que necesitabas.`,
    companyParagraph: `Nuestra pasión es brindar un servicio excepcional en discotecas y eventos, facilitando la compra de entradas, acceso VIP y bebidas de primera calidad. Con un equipo apasionado y comprometido, estamos aquí para hacer que tus noches sean épicas. Únete a nosotros y descubre la emoción detrás de la vida nocturna de la manera más conveniente y emocionante.`,
    versatileBrand: `Gestiona los ingresos por QR, control de puerta, venta de tickets y mucho + todo en un mismo lugar`,
    featureDescription: `La felicidad de entrar a tus lugares preferidos sin hacer colas interminables`,
  };

  import loguito from '/icons/loguito.png';
</script>

<section class="about-section">
  <div class="about-container">
    <div class="about-row">
      <div class="about-image">
        <img
          class="rounded-image"
          loading="lazy"
          src="/icons/doors.png"
          alt=""
        />
      </div>
      <div class="about-text">
        <div class="about-text-inner">
          <h2 class="about-title">¿Quienes somos?</h2>
          <p class="about-description">{aboutData.companyDescription}</p>
          <p class="about-paragraph">{aboutData.companyParagraph}</p>
          <div class="about-features">
            <div class="about-feature">
              <div class="feature-icon">
                <img src={loguito} alt="" srcset="">
              </div>
              <div class="feature-info">
                <h4 class="feature-title">SuperApp</h4>
                <p class="feature-description">{aboutData.versatileBrand}</p>
              </div>
            </div>
            <div class="about-feature">
              <div class="feature-icon">
                <img src={loguito} alt="" srcset="">
              </div>
              <div class="feature-info">
                <h4 class="feature-title">Sin espera</h4>
                <p class="feature-description">
                  {aboutData.featureDescription}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
