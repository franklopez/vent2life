<template>
  <div class="howItWorks">
    <div class="howItWorks__title">
      {{ $t('howItWorks.title') }}
    </div>
    <div class="howItWorks__list">
      <div class="howItWorks__list__item">
        <div class="howItWorks__list__item__image">
          <img alt="" src="~assets/repair_1.png">
        </div>
        <div class="howItWorks__list__item__text">
          {{ $t('howItWorks.text-1') }}
        </div>
      </div>
      <div class="howItWorks__list__item">
        <div class="howItWorks__list__item__image">
          <img alt="" src="~assets/repair_2b.png">
        </div>
        <div class="howItWorks__list__item__text">
          {{ $t('howItWorks.text-2') }}
        </div>
      </div>
      <div class="howItWorks__list__item">
        <div class="howItWorks__list__item__image">
          <img alt="" src="~assets/repair_3.png">
        </div>
        <div class="howItWorks__list__item__text">
          {{ $t('howItWorks.text-3') }}
        </div>
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
          path: '~assets/Repair_1.png'
        },
        {
          label: 'howItWorks.text-2',
          path: '~assets/Repair_2B.png'
        },
        {
          label: 'howItWorks.text-3',
          path: '~assets/Repair_3.png'
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
    background-color: rgb(255,202,110);
    height: 90vh;
  &__title {
    padding-top: 40px;
    color: white;
    font-size: 80px;
    text-align: center;
  }
  &__list {
    padding-top: 50px;
    display: flex;
    justify-content: space-evenly;
    &__item {
      width: 400px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      &__image {
        padding: 20px;
        background-color: rgba(79,79,79,.2);
        height: 320px;
        width: 320px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        img {
          height: 320px;
        }
      }
      &__text {
        color: white;
        font-size: 20px;
        text-align: center;
        padding-top: 50px;
        display: flex;
        justify-content: space-evenly;
      }
    }

  }
    &__text__list {
      color: white;
      font-size: 20px;
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
