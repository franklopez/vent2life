<template>
  <div class="home">
    <div class="home__ventilators">
      <div class="home__ventilators__counter">
        <div class="home__ventilators__counter__value">
          {{ vents.number }}
        </div>
        <div class="home__ventilators__counter__label">
          {{ $t(vents.label) }}
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      vents: {
        number: 55,
        label: 'header.ventilators'
      }
    }
  },
  head () {
    return { title: this.$t('home.title') }
  }
}
</script>
<style lang="scss">
  .home {
    height: 90vh;
    background-image: linear-gradient(#fff, #c0c0c0);
    &__ventilators {
      display: flex;
      justify-content: center;
      padding-top:20px;
      &__counter {
        width: 160px;
        height: 30px;
        display: flex;
        justify-content: space-evenly;
        color: white;
        background-color: #FC7D08;
        &__value {
          font-weight: bold;
        }
      }
    }
  }

</style>
