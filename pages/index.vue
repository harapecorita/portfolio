<template>
  <div>
    <Hello id="hello" />
    <Index class="index" text="Latest works" />
    <div id="cards-area">
      <div id="cards-grid">
        <Card
          v-for="(card, i) in getCards"
          :key="i"
          class="item"
          :thumbnail="card.thumbnail"
          :title="card.title"
          :tags="card.tags"
          :description="card.description"
          :infomations="card.infomations"
        />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
type Infomation = {
  title: Text;
  data: Text;
};
type Card = {
  thumbnail: Text;
  title: Text;
  tags: Text[];
  description: Text;
  infomations: Infomation[];
};
export default Vue.extend({
  data () {
    return {
      cards: (this as any).$t('cards')
    }
  },
  computed: {
    getCards (): Card[] {
      const cards: Card[] = []
      for (let i = 0; i < 3; i++) {
        cards.push(this.cards[i])
      }
      return cards
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
#cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(420px, 420px));
  justify-content: start;
  gap: 20px;
}
</style>
