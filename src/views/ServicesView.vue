<template>
  <main>
    <!--? Services Area Start -->
    <section class="service-area pb-170">
      <div class="container">
        <!-- Section Tittle -->
        <div class="row d-flex justify-content-center">
          <div class="col-xl-7 col-lg-8 col-md-11 col-sm-11">
            <div class="section-title text-center mb-90">
              <span>Les servives de l'association</span>
              <h2>Nous vous offrons la meilleure prise en charge possible</h2>
            </div>
          </div>
        </div>
        <!-- Section caption -->
        <div class="row">
          <div class="col-xl-4 col-lg-4 col-md-6">
            <div class="services-caption text-center mb-30">
              <div class="service-icon">
                <img src="@/assets/crash1.jpg" alt="..." />
              </div>
              <div class="service-cap">
                <h4>Aide aux victimes</h4>
                <p>
                  L'association a décidé de se mobiliser pour vous apporter la prise en change rapide.
                </p>
              </div>
            </div>
          </div>
          <div class="col-xl-4 col-lg-4 col-md-6">
            <div class="services-caption active text-center mb-30">
              <div class="service-icon">
                <img src="@/assets/crash2.jpg" alt="..." />
              </div>
              <div class="service-cap">
                <h4>Assistance et conseils</h4>
                <p>
                  Les victimes d'accidents de la route sont encourgées à contacter
          l'ASA pour recevoir de l'aide et des conseils.
                </p>
              </div>
            </div>
          </div>
          <div class="col-xl-4 col-lg-4 col-md-6">
            <div class="services-caption text-center mb-30">
              <div class="service-icon">
                <img src="@/assets/crash3.jpg" alt="..." />
              </div>
              <div class="service-cap">
                <h4>Actions de prévention</h4>
                <p>
                  Organisation des
          actions de sensibilisation, notamment auprès des jeunes conducteurs.
                </p>
              </div>
            </div>
          </div>
          <div class="col-xl-4 col-lg-4 col-md-6">
            <div class="services-caption text-center mb-30">
              <div class="service-icon">
                <img src="@/assets/crash4.jpg" alt="..." />
              </div>
              <div class="service-cap">
                <h4>Réseau de professionnel</h4>
                <p>
                  L'ASA met à la disposition des victimes un réseau de
          professionnel spécialisé.
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Services Area End -->
    <!-- Best Pricing Area Start -->
    <div class="best-pricing position-relative">
      <div class="container">
        <div class="row justify-content-end">
          <div class="col-xl-12 col-lg-12">
            <div class="section-title text-center mb-50">
              <span>Nos ressources</span>
              <h2>
                Les ressources de l'ASA<br />
                sont multiples!
              </h2>
            </div>
            <!-- Pricing  -->
            <div class="row">
              <!-- pricing list -->
              <div class="col-lg-6 col-md-6 col-sm-6">
                <div class="pricing-list">
                  <ul>
                    <li>Inscription personne. . . . . . . . . . . <span>1 000 FCFA</span></li>
                    <li>Inscription famille. . . . . . . . . . .<span>3 000 FCFA</span></li>
                    <li>Inscription entreprise. . . . . . . . . . .<span>5 000FCFA</span></li>
                  </ul>
                </div>
              </div>
              <div class="col-lg-6 col-md-6 col-sm-6">
                <div class="pricing-list">
                  <ul>
                    <li>Frais d'adhésion annuelle. . . . . . . . . . .<span>24 000 FCFA</span></li>
                    <li>Dons. . . . . . . . . . .<span>***FCFA</span></li>
                    <li>Subventions. . . . . . . . . . .<span>***FCFA</span></li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Best Pricing Area End -->

    <!-- Articles -->

    <div class="charte mt-5">
      <h2>Notre Charte         <span>téléchargez</span></h2>
      <!-- <a href="../assets/aavartc.pdf" target="_blank">Ouvrir le PDF</a> -->
      
        <div v-for="article in articles" :key="article.id" class="article-group">
          <h3 class="article-title">{{ article.title }}</h3>
          <ul class="section">
            <li v-for="paragraph in article.paragraphs" class="bullet-point" :key="paragraph.index">
              {{ paragraph }}
            </li>
          </ul>
        </div>
      
    </div>

    <!-- Articles End -->
  </main>
</template>

<script setup>
import { ref } from 'vue'

let articles = ref([
  {
    id: 1,
    title: 'Article 1 : constitution',
    paragraphs: [
      '(1) Il est créé en ce jour 16 mars 2024 en république du Cameroun, une association entre les adhérents aux présents statuts, et ceux qui y adhèreront ultérieurement.',
      "(2) L’assemblée générale adopte la dénomination de « L'Association de Solidarité en cas 'Accident ». Conformément à la loi du 01 juillet 1901 qui régit la liberté de création d’association.",
      "(3) L’association est à but non lucratif, apolitique, accueillant toutes personnes sans distinction d’âge, de sexe, de race de tribu, de culture ou de religion. Sa devise est PRISE EN CHARGE POUR TOUS, SAUVE DES VIES ET FAVORISE LA GUERISON"
    ]
  },
  {
    id: 2,
    title: 'Article 2 : but et objectifs',
    paragraphs: [
      "(1) : le but de l’Association de Solidarité en cas d'Accident est de : Faciliter les conditions d’accès à la prise en charge des victimes des accidents de la route dans les hôpitaux, formation sanitaires et cliniques.",
      '(2)L’objectif principal de l’association est de mener, aux moyens et ressources des cotisations des membres, des dons, des subventions et tous autres profits, des actions de prévoyance, d’accès aux soins faciles et réduire le taux de décès lié à la prise en charge tardive donc la raison est, le qui va payer la factures et examens de la victime. De manière spécifique, Promouvoir sur le plan social la prise en charge des personnes victimes d’accidents, Promouvoir et garantir la protection sociale, Réduire le taux de mortalité accidentel, Mettre en place les œuvres d’entraide, d’assistance et de prise en charge rapide'
    ]
  },
  {
    id: 3,
    title: 'Article 4 : durée illimitée'
  },
  {
    id: 4,
    title: 'Article 5 : Conditions d’adhésion',
    paragraphs: [
      'Accepter intégralement les statuts et le règlement intérieur de l’association.',
      'S’engager à prendre des responsabilités actives pour faciliter l’évolution de l’association',
      ' Être capable de s’acquitter des droits d’adhésion qui sont fixés à 1000fcfa l’inscription, et de la cotisation mensuelle volontaire par membre d’un montant de 2000 FCFA minimum.'
    ]
  },
  {
    id: 5,
    title: 'Article 22 : la provenance des ressources',
    paragraphs: [
      'Inscriptions, Cotisations mensuelles des membres, Participation des membres au frais de fonctionnement, Dons, Subventions, Autres profits à numéraires ou en nature des bienfaiteurs'
    ]
  },
  {
    id: 6,
    title: 'Article 23 : les modalités de prise charge',
    paragraphs: [
      '(1) Toute personne victime d’un accident de la route, qui est membre de cette association sera prise en charge suivant :',
      'Chaque membre aura une carte biomédicale contenant ses informations personnelles.',
      'Chaque victime dans un hôpital a droit à une prise en charge immédiate, et les premiers soins sont payés intégralement par l’association en fonction des disponibilités financières de la caisse',
      'L’association vient en aide en fonction des disponibilités financières des caisses de l’association',
      'La famille de la victime participe en collaboration avec l’association pour sauver la vie en danger et de s’acquitter des frais médicaux.'
    ]
  }
])
</script>

<style scoped>
.charte{
  padding: 5px 15px;
}
h2 {
  color: #333;
  font-size: 24px;
}
span{
  font-size: 12px;
  color: var(--primary);
}

.article-group{
  border: 1px solid var(--secondary);
  padding: 5px 10px;
  margin: 10px 0;
  border-radius: 10px;
}

.article-title {
  color: #666;
  font-size: 20px;
  margin-top: 30px;
}

ul.section {
  color: #333;
  font-size: 16px;
  list-style-type: none;
  padding-left: 20px;
}

.bullet-point {
  position: relative;
  padding-left: 15px;
}

.bullet-point:before {
  content: '•';
  position: absolute;
  left: 0;
  top: 0;
}

</style>
