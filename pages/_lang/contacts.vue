<template>
  <div class="Content">
    <div class="container">
      <h1 class="Content__Title">
        {{ $t('contacts.title') }}
      </h1>
      <p>{{ $t('contacts.introduction') }}</p>
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
