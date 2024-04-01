<template>
  <main>
    <!--? About Area Start -->
    <section class="about-area">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-6 col-md-11">
            <!-- about-img -->
            <div class="about-img">
              <img src="@/assets/crash5.jpg" alt="" />
            </div>
          </div>
          <div class="col-lg-6 col-md-12">
            <div class="about-caption">
              <!-- Section Tittle -->
              <div class="section-title mb-25">
                <span>A propos de notre association</span>
                <h2>Lorem ipsum dolor sit.!</h2>
              </div>
              <p class="mb-30 pera-bottom">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Commodi, dolorem in
                consequuntur cumque excepturi officiis explicabo eveniet magni ullam ut eos a natus
                repellendus, inventore ipsa aut culpa laborum! Unde.
              </p>
              <p class="pera-top mb-50">
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ea voluptatem quae vero
                eaque eligendi corrupti.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- About-2 Area End -->
    <!--? Team Start -->
    <div class="team-area pb-180">
      <div class="container">
        <!-- Section Tittle -->
        <div class="row justify-content-center">
          <div class="col-xl-8 col-lg-8 col-md-11 col-sm-11">
            <div class="section-title text-center mb-100">
              <span>Equipe Professionnelle</span>
              <h2>Lorem ipsum dolor sit amet consectetur.</h2>
            </div>
          </div>
        </div>

        <!-- single Tem -->
        <div id="carouselExampleCaptions" class="carousel slide">
          <div class="carousel-indicators">
            <button
              type="button"
              data-bs-target="#carouselExampleCaptions"
              data-bs-slide-to="0"
              class="active"
              aria-current="true"
              aria-label="Slide 1"
            ></button>
            <button
              type="button"
              data-bs-target="#carouselExampleCaptions"
              data-bs-slide-to="1"
              aria-label="Slide 2"
            ></button>
            <button
              type="button"
              data-bs-target="#carouselExampleCaptions"
              data-bs-slide-to="2"
              aria-label="Slide 3"
            ></button>
          </div>
          <div class="carousel-inner">
            <div class="carousel-item active">
              <img src="@/assets/crash6.jpg" class="d-block w-100 team-img" alt="..." />
              <div class="carousel-caption d-md-block team-caption text-center">
                <h5>First slide label</h5>
                <p>Some representative placeholder.</p>
              </div>
            </div>
            <div class="carousel-item">
              <img src="@/assets/crash7.jpg" class="d-block w-100" alt="..." />
              <div class="carousel-caption team-caption d-md-block text-center">
                <h5>Second slide label</h5>
                <p>Some representative placeholder.</p>
              </div>
            </div>
            <div class="carousel-item">
              <img src="@/assets/crash8.jpg" class="d-block w-100" alt="..." />
              <div class="carousel-caption team-caption d-md-block text-center">
                <h5>Third slide label</h5>
                <p>Some representative placeholder.</p>
              </div>
            </div>
          </div>
          <button
            class="carousel-control-prev"
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide="prev"
          >
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button
            class="carousel-control-next"
            type="button"
            data-bs-target="#carouselExampleCaptions"
            data-bs-slide="next"
          >
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
      </div>
    </div>
    <!-- Team End -->
    <div class="missions">
      <h1>Nos Missions</h1>
      <div class="mission">
        <p>
          Mission de L'AAVATC : l'association aide aux victimes d'accident de la route et de travail
          du Cameroun est dédiée à aider les victimes d'accident de la route, à faciliter la prise
          en charge dans les hôpitaux, financier les frais médicaux pour sauver les vies.
        </p>
      </div>
      <div class="mission">
        <p>
          Réseau de professionnel : L'AAVARTC met à la disposition des victimes un réseau de
          professionnel spécialisé, incluant les avocats en droit du dommage corporel, des experts
          médicaux, les psychologues, les autorités compétentes (police, gendarmerie nationale) pour
          soutenir les victimes dans toutes les étapes.
        </p>
      </div>
      <div class="mission">
        <p>
          Actions de prévention : en plus de son rôle d'accompagnement d'aide, l'association d'aide
          aux victimes des accidents de la route par le biais de l'auto-école italienne organise des
          actions de sensibilisation, notamment auprès des jeunes conducteurs.
        </p>
      </div>
      <div class="mission">
        <p>
          Assistance et conseils : les victimes d'accidents de la route sont encourgées à contacter
          l'AAVARTC pour recevoir de l'aide et des conseils.
        </p>
      </div>
      <div class="mission">
        <p>
          L'association d'aide aux victimes d'accidents de la route du Cameroun a pour vocation
          d'aider. Elle participe également à la commission des usagers de la route et fait des
          actions de prévention.
        </p>
        <P
          >L'association a décidé de se mobiliser pour vous apporter la prise en change rapide à
          votre situation. Si vous êtes victimes d'un accident de la route ou si vous avez des
          questions n'hésitez pas à contacter l'association d'aide aux victimes d'accident de la
          route et de travail du Cameroun pour obtenir de l'aide et des conseils.</P
        >
      </div>
      <div class="mission">
        <p>Association aide aux victimes : l'accident de la route et professionnels</p>
        <P
          >L'association propose des professionnels adhèrent tous aux principes de la charte de
          L'AAVARTC afin de fournir un travail humain, honnête et de qualité. Pour les
          professionnels souhaitent intervenir, il convient de laisser un message email à
          l'intention du président de l'association d'aide aux victimes d'accidents de la route dans
          la rubrique contact.</P
        >
      </div>
    </div>
  </main>
</template>

<style></style>
