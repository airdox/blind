<template>
  <div class="step">
    <img v-if="numero === 1" src="@/assets/icons/vase-icon.png" alt="icon">
    <img v-if="numero === 2" src="@/assets/icons/heart-icon.png" alt="icon">
    <img v-if="numero === 3" src="@/assets/icons/eye-icon.png" alt="icon">
    <img v-if="numero === 4" src="@/assets/icons/truck-icon.png" alt="icon">
    <p class="numero">
      .{{ numero }}
    </p>
    <p class="description">
      {{ description }}
    </p>
  </div>
</template>

<script>
export default {
  name: 'Step',
  props: {
    image: {
      type: String,
      default: '/'
    },
    numero: {
      type: Number,
      default: 1
    },
    description: {
      type: String,
      default: 'description'
    }
  }
}
</script>

<style lang="scss" scoped>

.step {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  width: 200px;
  text-align: center;

  &:first-child {
    transform: translateY(-23px);
  }

  .numero {
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: "Primary", sans-serif;
    font-size: 60px;
    color: rgba(0,0,0,0);
    -webkit-text-stroke-width: 1.5px;
    -webkit-text-stroke-color: black;
  }

  .description {
    color: black;
    font-size: 18px;
    padding-bottom: 20px;
  }
}

</style>
