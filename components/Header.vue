<template>
  <div class="header-wrapper">
    <div class="header-wrapper__logo">
      <img alt="" src="~assets/logo.png">
    </div>
    <div class="header-wrapper__menu">
      <div v-for="item in menu_items" :key="item.label">
        {{ item.label }}
      </div>
    </div>
    <div class="header-wrapper__buttons">
      <div class="header-wrapper__buttons__login">
        <button>Log in</button>
      </div>
      <div class="header-wrapper__buttons__counter">
        <div class="header-wrapper__buttons__counter__value">
          {{ vents.number }}
        </div>
        <div class="header-wrapper__buttons__counter__label">
          {{ vents.label }}
        </div>
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
        label: 'Ventiladores'
      },
      menu_items: [
        {
          label: 'About',
          jummp: ''
        },
        {
          label: 'How it works',
          jummp: ''
        },
        {
          label: 'Our Team',
          jummp: ''
        },
        {
          label: 'Contact',
          jummp: ''
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
    }
    &__buttons {
      width: 30%;
      display: flex;
      justify-content: space-evenly;
      align-items: center;
      &__login {
        button {
          width: 181px;
          background-color: white;
          border-color: #009ea6;
          border-radius: 25px;
        }
       }
      &__counter {
        width: 156px;
        height: 28px;
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
