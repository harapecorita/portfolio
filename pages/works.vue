<template>
  <div id="cards-area">
    <CardsGrid :cards="cards" />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  data () {
    return {
      cards: (this as any).$t('cards')
    }
  },
  head () {
    return {
      title: 'works'
    }
  }
})
</script>

<style scoped>
#cards-area {
  margin-top: 60px;
}
</style>
