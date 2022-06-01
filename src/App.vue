<template>
  <div id="app">
    <keep-alive exclude="Detail"><!--所以的页面都会被缓存，只有Detail这个不会被缓存-->
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style></style>
