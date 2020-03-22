<template>
  <div id="companies" class="companies">
    <div class="companies__wrapper">
      <div class="companies__wrapper__title">
        {{ $t('companies.title') }}
      </div>
      <div class="companies__wrapper__sub-title">
        {{ $t('companies.sub-title') }}
      </div>
    </div>
    <div class="companies__list">
      <div class="companies__list__logo">
        <img src="~assets/logo.png">
      </div>
      <div class="companies__list__logo">
        <img src="~assets/logo.png">
      </div>
      <div class="companies__list__logo">
        <img alt="" src="~assets/logo.png">
      </div>
      <div class="companies__list__logo">
        <img alt="" src="~assets/logo.png">
      </div>
      <div class="companies__list__logo">
        <img alt="" src="~assets/logo.png">
      </div>
      <div class="companies__list__logo">
        <img alt="" src="~assets/logo.png">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head () {
    return { title: this.$t('companies.title') }
  }
}
</script>
<style lang="scss">
  .companies {
    height: 90vh;
    &__wrapper {
      margin-top: 10px;
      font-size: 50px;
      &__title {
        font-weight: bold;
        margin-left: 10vw;
      }
      &__sub-title {
        margin-left: 20vw;
      }
    }
    &__list{
      margin-top: 20px;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-evenly;
      &__logo {
        img {
          width: 450px;
        }
      }
    }
  }

</style>
