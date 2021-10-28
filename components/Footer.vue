<template>
  <footer class="footer">
    <div>
      <h2>blind</h2>
    </div>
    <section class="informations">
      <div class="all-links">
        <div class="links">
          <h3>À propos</h3>
          <ul>
            <li class="link">
              <NuxtLink to="/">
                Le concept
              </NuxtLink>
            </li>
            <li class="link">
              <NuxtLink to="/">
                L'équipe
              </NuxtLink>
            </li>
          </ul>
        </div>
        <div class="links">
          <h3>Infos</h3>
          <ul>
            <li class="link">
              <NuxtLink to="/">
                Retour et remboursement
              </NuxtLink>
            </li>
            <li class="link">
              <NuxtLink to="/">
                FAQ
              </NuxtLink>
            </li>
          </ul>
        </div>
        <div class="links">
          <h3>Artistes</h3>
          <ul>
            <li class="link">
              <NuxtLink to="/">
                Travailler avec blind
              </NuxtLink>
            </li>
            <li class="link">
              <NuxtLink to="/">
                Les actualités
              </NuxtLink>
            </li>
          </ul>
        </div>
      </div>
      <div class="contacts">
        <h3>Nous contacter</h3>
        <div class="social-networks">
          <img src="@/assets/icons/facebook-icon.png" alt="facebook-icon">
          <img src="@/assets/icons/instagram-icon.png" alt="instagram-icon">
          <img src="@/assets/icons/twitter-icon.png" alt="twitter-icon">
        </div>
      </div>
    </section>
  </footer>
</template>

<style lang="scss" scoped>
@import '@/assets/css/main';
@import '@/assets/css/components/Footer/main';
</style>
