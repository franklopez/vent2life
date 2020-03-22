<template>
  <div id="home" class="home">
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
    <div class="home__title">{{ $t('home.title') }}</div>
    <div class="home__wrapper">
      <div class="home__wrapper__sub-title">{{ $t('home.sub-title') }}</div>
      <div class="home__wrapper__description">{{ $t('home.description') }}</div>
      <div class="home__wrapper__sign-up">
        <NuxtLink :to="$i18n.path('signUp')" class="Header__Link" active-class="none" exact>
          {{ $t('header.signUp') }}
        </NuxtLink>
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
    background-image: linear-gradient(#ffffff, #00a89c);
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
    &__title {
      font-size: 50px;
      margin-left: 30vw;
    }
    &__wrapper {
      width: 650px;
      margin: auto;
    &__sub-title {
       font-size: 50px;
       font-weight: bold;
     }
     &__description {
        margin-top: 15px;
     }
      &__sign-up {
        margin-top: 15px;
        display: flex;
        justify-content: flex-end;
        a {
          display: block;
          width: 200px;
          text-align: center;
          background-color: #009ea6;
          color: #fff;
          border-radius: 25px;
        }
      }
    }
  }

</style>
