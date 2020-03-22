<template>
  <div id="ourTeam" class="ourTeam">
    <div class="container">
      <h1 class="Content__Title">
        {{ $t('ourTeam.title') }}
      </h1>
      <p>{{ $t('ourTeam.introduction') }}</p>
    </div>
  </div>
</template>

<script>
export default {
  head () {
    return { title: this.$t('home.title') }
  }
}
</script>
