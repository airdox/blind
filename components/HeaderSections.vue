<template>
  <section class="headers">
    <Header :fixed="false" :mode="'light'" />
    <Header :fixed="true" :mode="'light'" />
  </section>
</template>

<script>
import Header from './Header.vue'

export default {
  components: {
    Header
  }
}
</script>
