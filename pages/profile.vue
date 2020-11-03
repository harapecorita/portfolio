<template>
  <div id="profile">
    <h3 class="name">{{ $t("profile.name") }}</h3>
    <p class="birth">{{ $t("profile.birthday") }}</p>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

export default Vue.extend({});
</script>

<style scoped>
#profile {
  padding-top: 60px;
}
.name {
  font-size: 22px;
  color: #0f2540;
}
.birth {
  font-size: 12px;
  color: #6f7c8c;
}
</style>
