<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    city
  </div>
</template>

<script>
import cityHeader from './components/Header'
import citySearch from './components/Search'

export default {
  name: 'City',
  components: {
    cityHeader,
    citySearch
  }
}
</script>

<style lang="stylus" scoped>

</style>
