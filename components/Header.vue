<template>
  <header
    :class="
      'header' +
        (fixed ? '-fixed' : '') +
        (absolute ? '-absolute' : '') +
        ' ' +
        mode
    "
  >
    <div class="container">
      <div class="wrapper">
        <div class="header-item-left">
          <NuxtLink
            to="/"
            class="brand"
          >
            <img src="/Logo-small.svg" alt="logo-small">
          </NuxtLink>
        </div>
        <!-- Section: Navbar Menu -->
        <div class="header-item-center">
          <div class="overlay" @click="toggleMenu" />
          <nav class="menu">
            <div class="menu-mobile-header">
              <button
                type="button"
                class="menu-mobile-close"
                @click="toggleMenu"
              >
                <v-icon color="black">
                  mdi-close
                </v-icon>
              </button>
            </div>
            <ul class="menu-section">
              <div class="links">
                <li>
                  <NuxtLink to="/">
                    Surprenez-moi
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">
                    Artistes
                  </NuxtLink>
                </li>
                <li>
                  <NuxtLink to="/">
                    Galeries
                  </NuxtLink>
                </li>
              </div>
            </ul>
          </nav>
        </div>

        <div class="header-item-right">
          <div class="other-links">
            <NuxtLink
              to="/"
            >
              <img src="@/assets/icons/basket-icon.png" alt="'user-icon'">
              <p>Mon panier</p>
            </NuxtLink>
            <NuxtLink
              to="/"
            >
              <img src="@/assets/icons/user-icon.png" alt="'user-icon'">
              <p>Mon compte</p>
            </NuxtLink>
          </div>
          <button type="button" class="menu-mobile-trigger" @click="toggleMenu">
            <span />
            <span />
            <span />
            <span />
          </button>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  props: {
    fixed: Boolean,
    absolute: Boolean,
    mode: {
      type: String,
      default: 'light'
    }
  },
  beforeMount () {
    window.addEventListener('scroll', this.menuFixed)
  },
  beforeDestroy () {
    window.removeEventListener('scroll', this.menuFixed)
  },
  methods: {
    toggleMenu () {
      document.querySelector('.menu').classList.toggle('active')
      document.querySelector('.menu .menu-section').classList.toggle('active')
    },
    menuFixed () {
      const header = document.getElementsByClassName('header-fixed')[0]
      if (window.scrollY >= 200) {
        header.classList.add('show')
      } else {
        header.classList.remove('show')
      }
    }
  }
}
</script>

<style lang="scss" scoped>
@import './assets/css/main';
@import './assets/css/components/Header/main';
</style>
