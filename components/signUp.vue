<template>
<div class="sign-up">
  <div class="sign-up__list">
    <div class="sign-up__list__item">
      <div class="sign-up__list__item__icon">
        <img src="~assets/Icon-Hospital.png" alt="">
      </div>
      <div class="sign-up__list__item__label">
        {{ $t(entities[0].label) }}
      </div>
      <div class="sign-up__list__item__description">
        {{ $t(entities[0].description) }}
      </div>
      <div class="sign-up__list__item__caption">
        <a class="Header__Link" active-class="none" :href="entities[0].path">{{ $t(entities[0].caption) }}</a>
      </div>
    </div>
    <div class="sign-up__list__item">
    <div class="sign-up__list__item__icon">
      <img src="~assets/Icon-Empresas.png" alt="">
    </div>
    <div class="sign-up__list__item__label">
      {{ $t(entities[1].label) }}
    </div>
    <div class="sign-up__list__item__description">
      {{ $t(entities[1].description) }}
    </div>
    <div class="sign-up__list__item__caption">
      <a class="Header__Link" :href="entities[1].path">{{ $t(entities[1].caption) }}</a>
    </div>
  </div>
    <div class="sign-up__list__item">
    <div class="sign-up__list__item__icon">
      <img src="~assets/Icon-Voluntario.png" alt="">
    </div>
    <div class="sign-up__list__item__label">
      {{ $t(entities[2].label) }}
    </div>
    <div class="sign-up__list__item__description">
      {{ $t(entities[2].description) }}
    </div>
    <div class="sign-up__list__item__caption">
      <a class="Header__Link" :href="entities[2].path">{{ $t(entities[2].caption) }}</a>
    </div>
  </div>
  </div>
</div>
</template>

<script>
export default {
  data () {
    return {
      entities: [
        {
          label: 'signUp.label-1',
          icon: '~assets/Icon-Hospital.png',
          description: 'signUp.description_1',
          caption: 'signUp.caption_1',
          path: 'http://sapo.pt'
        },
        {
          label: 'signUp.label-2',
          icon: '~assets/Icon-Empresas.png',
          description: 'signUp.description_2',
          caption: 'signUp.caption_2',
          path: 'http://sapo.pt'
        },
        {
          label: 'signUp.label-3',
          icon: '~assets/Icon-Voluntario.png',
          description: 'signUp.description_3',
          caption: 'signUp.caption_3',
          path: 'http://sapo.pt'
        }
      ]
    }
  },
  head () {
    return { title: this.$t('signUp.title') }
  }
}
</script>

<style lang="scss" scoped>
  .sign-up {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    background-color: #90d3ce;
    height: 90vh;
    &__list{
      display: flex;
      width: 90vw;
      align-items: center;
      justify-content: space-evenly;
      &__item {
        display: flex;
        flex-direction: column;
        height: 436px;
        width: 384px;
        align-items: center;
        justify-content: space-evenly;
        background-color: white;
        &__icon {
          img {
            width: 90px;
            height: 90px;
          }
        }
        &__label {
          font-size: 30px;
          font-weight: bold;
        }
        &__description {
          text-align: center;
        }
        &__caption {
          a {
            display: block;
            width: 300px;
            text-align: center;
            background-color: #009ea6;
            color: #fff;
            border-radius: 25px;
          }
        }
      }
      &__item:last-of-type {
        background-image: url('~assets/Patern-white.png');
        background-size: 100% ;
      }
    }
  }
</style>
