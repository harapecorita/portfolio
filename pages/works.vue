<template>
  <div>
    <div id="cards-area">
      <div id="cards-grid">
        <Card
          v-for="(card, i) in cards"
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
import Vue from "vue";

export default Vue.extend({
  data() {
    return {
      cards: (this as any).$t("cards"),
    };
  },
  head() {
    return {
      title: "works",
    };
  },
});
</script>

<style scoped>
#cards-area {
  margin-top: 60px;
}
#cards-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(420px, 420px));
  justify-content: start;
  gap: 20px;
}
</style>
