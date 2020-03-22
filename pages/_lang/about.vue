<template>
  <div class="about">
    <div class="about__project">
      <div class="about__project__title">
        {{ $t('about.title') }}
      </div>
      <div class="about__project__sub-title">
        {{ $t('about.sub-title') }}
      </div>
    </div>
    <div class="about__description">
      <div class="about__description__line">
        {{ $t('about.description-1') }}
      </div>
      <div class="about__description__line">
        {{ $t('about.description-2') }}
      </div>
      <div class="about__description__line">
        {{ $t('about.description-3') }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  head () {
    return { title: this.$t('about.title') }
  }
}
</script>
<style lang="scss">
  .about {
    display: flex;
    justify-content: space-evenly;
    height: 90vh;
    background-image: url('~assets/medic.png');
    background-color: #3fbfb6;
    background-repeat: no-repeat;
    background-position: 30% 50%;
    &__project {
      width: 400px;
      margin-top: 250px;
      font-size: 70px;
      &__title {
        font-weight: bold;
      }
    }
    &__description {
      width: 600px;
      font-size: 20px;
      margin-top: 250px;
      &__line {
        padding: 15px;
      }
    }
  }

</style>
