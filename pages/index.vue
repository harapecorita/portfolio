<template>
  <div>
    <Hello id="hello" />
    <Index class="index" text="Latest works" />
    <div id="card-area">
      <CardsGrid :cards="cards" :cards-number="3" />
      <MoreButton
        title="goto works"
        :path="localePath('/works')"
        class="more-button"
      />
    </div>
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
      title: 'hello'
    }
  }
})
</script>

<style scoped>
#hello {
  padding-top: 60px;
}
.index {
  margin-top: 40px;
}
#card-area{
  position: relative;
  padding-bottom: 30px;
}
.more-button {
  margin-top: 14px;
}
</style>
