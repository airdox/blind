<template>
  <div class="homepage">
    <section class="hero">
      <h1>blind</h1>
      <h2>laissez-vous guider par vos émotions</h2>
    </section>
    <section class="what_is_it">
      <h2>Blind qu'est-ce que c'est ?</h2>
      <p>Blind est une start-up créée par plusieurs passionés d’art visuels qui se sont donné pour mission de mettre en avant les petits créateurs et faire découvrir l’art au plus grand nombre. Que ce soit dans la peinture, la photographie, la sculpture ou encore les mangas,
        Blind vous propose une sélection personnalisée en fonction des émotions que vous souhaitez ressentir. </p>
    </section>
    <section class="how_does_it_work">
      <h2>Comment ça fonctionne ?</h2>
      <div class="steps">
        <Step v-for="(step, index) in steps" :key="index" :numero="index + 1" :description="step.description" />
      </div>
      <NuxtLink
        to="/"
      >
        <v-btn depressed class="btn light">
          Surprenez-moi
        </v-btn>
      </NuxtLink>
    </section>
    <section class="discover">
      <h2>Découvrez nos artistes</h2>
      <div class="artists-list">
        <div class="artist">
          <img src="@/assets/images/anais.png" alt="anais">
          <p class="name">Anaïs Chesnay</p>
          <p class="job">Artiste numérique</p>
        </div>
        <div class="artist">
          <img src="@/assets/images/theodore.png" alt="anais">
          <p class="name">Anaïs Chesnay</p>
          <p class="job">Peintre</p>
        </div>
        <div class="artist">
          <img src="@/assets/images/olivier.png" alt="anais">
          <p class="name">Anaïs Chesnay</p>
          <p class="job">Peintre</p>
        </div>
      </div>
      <NuxtLink
        to="/"
      >
        <v-btn depressed class="btn light">
          Soutenir nos artistes
        </v-btn>
      </NuxtLink>
    </section>
    <section class="donation">
      <h2>Vous voulez faire un don à un artiste ?</h2>
      <p>
        Chez Blind nous mettons en avant des artistes qui ont peu de visibilité.
        C’est pourquoi de soutenir l’artiste de votre choix, en échange vous recevrez une oeuvre de l’artiste que vous avez choisi correspondant au montant que vous lui avez offert.
      </p>
    </section>
  </div>
</template>

<script>
import Step from '~/components/Step.vue'

export default {
  components: {
    Step
  },
  data () {
    return {
      steps: [
        {
          description: 'Choisissez une catégorie de produit'
        },
        {
          description: 'Sélectionnez \n' +
            'la signification \n' +
            'de votre oeuvre'
        },
        {
          description: 'Commandez et découvrez l’oeuvre chez vous'
        },
        {
          description: 'Si elle ne vous plait pas, retournez-la gratuitement'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import './assets/css/main';
@import './assets/css/pages/homepage/main';
</style>
