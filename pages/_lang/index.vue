<template>
  <div>
    <home />
    <about />
    <howItWorks />
    <signUp />
    <team />
    <companies />
    <contacts />
  </div>
</template>
<script>
import home from '~/components/home'
import about from '~/components/about'
import howItWorks from '~/components/howItWorks'
import signUp from '~/components/signUp'
import team from '~/components/ourTeam'
import companies from '~/components/companies'
import contacts from '~/components/contacts'

export default {
  components: {
    home,
    about,
    howItWorks,
    signUp,
    team,
    companies,
    contacts
  }
}
</script>
