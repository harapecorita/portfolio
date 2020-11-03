<template>
  <div id="header">
    <nuxt-link :to="localePath('/')">
      <h1 class="title">Muto Tsujimoto</h1>
    </nuxt-link>
    <Navigation />
  </div>
</template>

<style scoped>
#header {
  width: 300px;
  text-align: left;
  position: fixed;
  left: 0;
  top: 0;
  padding: 30px;
}
.title {
  font-size: 22px;
  margin: 30px 0 30px 0;
  color: #0f2540;
}
</style>