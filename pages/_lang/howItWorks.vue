<template>
  <div class="Content">
    <div class="container">
      <h1 class="Content__Title">
        {{ $t('howItWorks.title') }}
      </h1>
      <p>{{ $t('howItWorks.introduction') }}</p>
    </div>
  </div>
</template>

<script>
export default {
  head () {
    return { title: this.$t('howItWorks.title') }
  }
}
</script>
