<template>
  <div class="card">
    <img
      :src="require('~/assets/' + thumbnail)"
      alt="thumbnail"
      class="image"
    >
    <div class="card-content">
      <div class="title">
        <span class="text">
          {{ title }}
        </span>
        <div v-if="tags != undefined" class="tag-box">
          <div v-for="(tag, i) in tags" :key="i" class="tag">
            <span>{{ tag }}</span>
          </div>
        </div>
      </div>
      <div v-if="description != ''" class="description">
        {{ description }}
      </div>
      <div v-if="infomations != []" class="infomations">
        <table>
          <tr v-for="(infomation, i) in infomations" :key="i">
            <td class="title">
              {{ infomation.title }}
            </td>
            <td>{{ infomation.data }}</td>
          </tr>
        </table>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue, { PropType } from 'vue'
type Infomation = {
  title: Text;
  data: Text;
};
export default Vue.extend({
  props: {
    thumbnail: {
      type: Text,
      required: true
    },
    title: {
      type: Text,
      required: true
    },
    tags: {
      type: Array as PropType<Text[]>,
      required: true
    },
    description: {
      type: Text,
      default: '',
      required: false
    },
    infomations: {
      type: Array as PropType<Infomation[]>,
      default: [],
      required: false
    }
  }
})
</script>

<style scoped>
.card {
  background: #ffffff;
  width: 420px;
}
.image {
  background: #6f7c8c;
}
.card-content {
  padding: 20px;
}
.title {
  display: flex;
}
.text {
  font-size: 16px;
  color: #0f2540;
  font-weight: 700;
}
.tag-box {
  display: flex;
  margin-left: 10px;
}
.tag {
  margin-left: 10px;
  height: 24px;
  line-height: 20px;
  background: #c9e1ec;
  border: 1px solid #3a8fb7;
  border-radius: 2px;
  padding: 0 8px 0 8px;
}
.tag span {
  font-size: 12px;
  color: #3a8fb7;
}
.description {
  color: #0f2540;
  font-size: 14px;
  margin-top: 16px;
}
.infomations {
  margin-top: 12px;
}
.infomations td {
  font-size: 12px;
  color: #6f7c8c;
}
.infomations .title {
  width: 130px;
}
</style>
