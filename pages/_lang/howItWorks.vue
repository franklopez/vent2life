<template>
  <div class="howItWorks">
    <div class="howItWorks__title">
      {{ $t('howItWorks.title') }}
    </div>
    <div class="howItWorks__image__list">
      <div class="howItWorks__image__list__item">
        <img alt="" src="~assets/repair_1.png">
      </div>
      <div class="howItWorks__image__list__item">
        <img alt="" src="~assets/repair_2.png">
      </div>
      <div class="howItWorks__image__list__item">
        <img alt="" src="~assets/repair_3.png">
      </div>
    </div>
    <div class="howItWorks__text__list">
      <div class="howItWorks__text__list__item">
        {{ $t('howItWorks.text-1') }}
      </div>
      <div class="howItWorks__text__list__item">
        {{ $t('howItWorks.text-2') }}
      </div>
      <div class="howItWorks__text__list__item">
        {{ $t('howItWorks.text-3') }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      repairs: [
        {
          text: 'howItWorks.text-1',
          path: '~assets/repair_1.png'
        },
        {
          label: 'howItWorks.text-2',
          path: '~assets/repair_2.png'
        },
        {
          label: 'howItWorks.text-3',
          path: '~assets/repair_3.png'
        }
      ]
    }
  },
  head () {
    return { title: this.$t('howItWorks.title') }
  }
}
</script>

<style lang="scss" scoped>
  .howItWorks {
    background-color: #F2A55E;
    height: 90vh;
  &__title {
    padding-top: 40px;
    color: white;
    font-size: 80px;
    text-align: center;
  }
  &__image__list {
    padding-top: 50px;
    display: flex;
    justify-content: space-evenly;
    &__item {
      padding: 20px;
      // background-color: white;
      height: 400px;
      width: 400px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      img {
        height: 320px;
      }
    }
  }
    &__text__list {
      color: white;
      text-align: center;
      padding-top: 50px;
      display: flex;
      justify-content: space-evenly;
      &__item {
        width: 400px;
        display: flex;
        justify-content: center;
      }
    }
}
</style>
