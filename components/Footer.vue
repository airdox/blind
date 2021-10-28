<template>
  <footer class="footer">
    <section class="informations">
      <div class="links">
        <h2>Liens</h2>
        <ul>
          <li class="link">
            <NuxtLink to="/starter">
              Bien débuter
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/games">
              Jeux
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/rules">
              Règles
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/characters/list">
              Personnages
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/news">
              Actualités
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/login">
              Se connecter
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/registration">
              S'inscrire
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/reservation">
              Réserver
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink to="/cgu">
              Condition d'utilisation
            </NuxtLink>
          </li>
          <li class="link">
            <NuxtLink
              to="/privacy_policy"
            >
              Politique de confidentialité
            </NuxtLink>
          </li>
        </ul>
      </div>
      <div class="contacts">
        <h2>Contact</h2>
        <address>
          <div class="contact">
            <v-icon color="white">
              mdi-phone
            </v-icon><a href="tel:0000000000">00 00 00 00 00</a>
          </div>
          <div class="contact">
            <v-icon color="white">
              mdi-at
            </v-icon><a href="mailto:support@nozenorpg.com">support@nozenorpg.com</a>
          </div>
          <div class="contact">
            <v-icon color="white">
              mdi-map-marker
            </v-icon><a
              class="contact"
              target="_blank"
              href="https://maps.google.com/?q=114 rue Clement Marot, Paris 93380"
            >114 rue Clement Marot, Paris 93380</a>
          </div>
        </address>
      </div>
    </section>
    <hr>
    <section class="social-networks">
      <a
        href="https://twitter.com/nozenopoint"
        target="_blank"
      ><v-icon>mdi-twitter</v-icon></a>
      <a
        href="https://www.youtube.com/channel/UCGxwEdu8TVnKjMVyyQeM5rA"
        target="_blank"
      ><v-icon>mdi-youtube</v-icon></a>
      <a
        href="https://discord.gg/CWR4UFeyDe"
        target="_blank"
      ><v-icon>mdi-discord</v-icon></a>
    </section>
    <section class="copyright">
      <p>© 2021 Nozeno - NozenoRPG Tout droits réservés</p>
    </section>
  </footer>
</template>

<script>
export default {
  data () {
    return {
      clusterStyle: [
        {
          url: '/logo.png',
          width: 56,
          height: 56,
          textColor: '#fff'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/css/main';
@import '@/assets/css/components/Footer/main';
</style>

<style>
footer .GMap__Wrapper {
  height: 200px !important;
  width: 100%;
}
</style>
