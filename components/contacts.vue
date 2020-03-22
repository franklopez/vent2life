<template>
  <div id="contacts" class="footer">
    <div class="footer__container">
      <div class="footer__container__contacts">
        <div class="footer__container__contacts__wrapper">
          <div class="footer__container__contacts__wrapper__title">
            {{ $t('contacts.title') }}
          </div>
          <div class="footer__container__contacts__wrapper__social">
            <div class="footer__container__contacts__wrapper__social__icon">
              <img src="~assets/Icon-Linkedin-White.png">
            </div>
            <div class="footer__container__contacts__wrapper__social__icon">
              <img src="~assets/Icon-Twiter-White.png">
            </div>
            <div class="footer__container__contacts__wrapper__social__address">
              <div>{{ $t('contacts.address.name') }}</div>
              <div>{{ $t('contacts.address.street') }}</div>
              <div>{{ $t('contacts.address.cp') }}</div>
              <div>{{ $t('contacts.address.country') }}</div>
            </div>
          </div>
        </div>
      </div>
      <div class="footer__container__legal">
        <div class="footer__container__legal__wrapper">
          <div class="footer__container__legal__wrapper__terms-conditions">
            {{ $t('contacts.legal') }} |  {{ $t('contacts.privacy') }}
          </div>
        </div>
      </div>
    </div>
    <div class="footer__copywrite">
      {{ $t('contacts.copywrite') }}
    </div>
  </div>
</template>

<script>
export default {
  head () {
    return { title: this.$t('contacts.title') }
  }
}
</script>
<style lang="scss" scoped>
  .footer {
    background-color: #009ea6;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    &__container{
      display: flex;
      justify-content: space-between;
      &__contacts {
        &__wrapper {
          &__title {
            color: white;
            padding: 50px 0 0 70px;
          }
          &__social {
            height: 200px;
            width: 450px;
            display: flex;
            align-items: center;
            justify-content: space-evenly;
            &__icon{
              img{
                width: 50px;
              }
            }
            &__address {
              // color: white;
            }
          }
        }
      }
      &__legal{
        &__wrapper{
          height: 300px;
          width: 450px;
          display: flex;
          flex-direction: column;
          justify-content: center;
          align-items: flex-end;
          &__terms-conditions{
            padding-right: 30px;
          }
        }
      }
    }
    &__copywrite {
      align-self: flex-end;
      padding: 0 30px 30px 0;
    }
  }
</style>
