<template>
  <div class="header-wrapper">
    <div class="header-wrapper__logo">
      <img alt="" src="/img/logo.png">
    </div>
    <div class="header-wrapper__menu">
      <NuxtLink v-for="item in menu_items" :key="item.label" :to="{path: '', hash: item.path}" v-scroll-to="{el: item.anchor}" exact>
        {{ $t(item.label) }}
      </NuxtLink>
    </div>
    <div class="header-wrapper__buttons">
      <div class="header-wrapper__buttons__login">
        <a class="Header__Link" href="https://sapo.pt">{{$t('header.logIn')}}</a>
      </div>
      <div class="header-wrapper__buttons__lang">
        <NuxtLink v-if="$i18n.locale === 'en'" :to="`/pt` + $route.fullPath" class="Header__Link" active-class="none" exact>
          {{ $t('header.portuguese') }}
        </NuxtLink>
        <NuxtLink v-else :to="$route.fullPath.replace(/^\/[^\/]+/, '')" class="Header__Link" active-class="none" exact>
          {{ $t('header.english') }}
        </NuxtLink>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      vents: {
        number: 55,
        label: 'header.ventilators'
      },
      menu_items: [
        {
          label: 'header.about',
          path: 'about',
          anchor: '#about'
        },
        {
          label: 'header.howItWorks',
          path: 'howItWorks',
          anchor: '#howItWorks'
        },
        {
          label: 'header.ourTeam',
          path: 'ourTeam',
          anchor: '#ourTeam'
        },
        {
          label: 'header.companies',
          path: 'companies',
          anchor: '#companies'
        },
        {
          label: 'header.contacts',
          path: 'contacts',
          anchor: '#contacts'
        }
      ]
    }
  },
  methods: {
  }
}
</script>

<style lang="scss" scoped>
  .header-wrapper {
    background-color: white;
    position: -webkit-sticky;
    position: sticky;
    top: 0;
    z-index: 999;
    border: solid 1px #c0c0c0;
    padding: 20px 10px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    &__logo {
      img {
        height: 45px;
      }
    }
    &__menu {
      width: 30%;
      display: flex;
      justify-content: space-between;
      align-items: center;
      a {
        text-decoration: none;
        color: black;
      }
      a:hover {
        text-decoration: underline;
      }
    }
    &__buttons {
      width: 30%;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      &__lang {
        a {
          color:black;
          background-color: white;
          text-transform: uppercase;
          border-color: #009ea6;
          border-radius: 25px;
        }
      }
      &__signUp {
        a {
          background-color: #009ea6;
          color: #fff;
          border-radius: 25px;
        }
      }
      &__login {
        a {
          color:black;
          background-color: white;
          border-color: #009ea6;
          border-radius: 25px;
        }
      }
      &__counter {
        border-radius: 25px;
        min-width: 160px;
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
