<template>
  <div id="sidebar">
    <nuxt-link :to="localePath('/')">
      <h1 class="title">
        Muto Tsujimoto
      </h1>
    </nuxt-link>
    <Navigation />
  </div>
</template>

<style scoped>
#sidebar {
  text-align: left;
  padding: 20px;
}
.title {
  font-family: 'Roboto Mono', monospace;
  font-size: 22px;
  margin: 40px 0 40px 0;
  color: #0f2540;
}
</style>
